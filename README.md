# Semantic-search-with-chromaDB
A Python-based School Knowledge Assistant using ChromaDB for semantic search, enabling natural language queries to retrieve the most relevant school documents.
import chromadb
from chromadb.utils.embedding_functions import SentenceTransformerEmbeddingFunction

# Create embedding function
embedding_function = SentenceTransformerEmbeddingFunction(
    model_name="all-MiniLM-L6-v2"
)

# Persistent client
client = chromadb.PersistentClient(path="./school_db")

# Collection
collection = client.get_or_create_collection(
    name="school_documents",
    embedding_function=embedding_function
)

documents = [

# =========================
# Admissions
# =========================

"Admissions are open from January to March every year.",
"Students must submit their birth certificate, previous school result, and passport-size photographs for admission.",
"Admission forms are available at the school reception and on the official school website.",
"The admission office is open from Monday to Friday between 9:00 AM and 1:00 PM.",
"Scholarships are awarded to students with outstanding academic performance.",
"Students must pass the admission test before final enrollment.",

# =========================
# Academics
# =========================

"School timings are from 8:00 AM to 2:00 PM from Monday to Friday.",
"Monthly tests are conducted during the last week of every month.",
"Midterm examinations are held in October every year.",
"Final examinations are conducted at the end of the academic session.",
"Students must maintain at least 80 percent attendance to appear in the final examination.",
"Homework should be submitted before the assigned deadline.",
"Teachers provide weekly quizzes to assess student performance.",
"Report cards are distributed after every term examination.",

# =========================
# Library
# =========================

"The school library contains more than 15,000 books.",
"Students may borrow two books for a maximum of seven days.",
"The library remains open from 8:30 AM to 4:00 PM.",
"Students should maintain silence inside the library.",
"Reference books cannot be taken outside the library.",

# =========================
# Laboratories
# =========================

"The computer laboratory has high-speed internet and modern computers.",
"Students attend computer practical classes twice a week.",
"The science laboratory is equipped for Physics, Chemistry, and Biology experiments.",
"Students must wear laboratory coats during science practicals.",
"Laboratory equipment should be handled carefully.",

# =========================
# School Facilities
# =========================

"The school provides transport facilities on selected routes.",
"The school cafeteria serves healthy meals and clean drinking water.",
"Medical first aid is available in the school clinic.",
"The school has separate playgrounds for different sports.",
"Indoor games are available during break time.",

# =========================
# Rules & Policies
# =========================

"Students must wear the complete school uniform every day.",
"Mobile phones are not allowed during school hours.",
"Students should arrive at school at least fifteen minutes before assembly.",
"Late arrival without a valid reason may result in disciplinary action.",
"Students should respect teachers, classmates, and school staff.",
"Bullying and fighting are strictly prohibited on campus.",
"Students should keep classrooms clean and protect school property.",

# =========================
# Parents & Communication
# =========================

"Parent Teacher Meetings are held on the first Saturday of every month.",
"Parents can meet teachers after making an appointment.",
"Important announcements are shared through the school website and notice board.",
"Parents receive SMS notifications regarding important school updates.",

# =========================
# Fees
# =========================

"School fees must be paid before the 10th of every month.",
"A late fee is charged after the due date.",
"Fee vouchers are available from the accounts office and online portal.",

# =========================
# Activities
# =========================

"The school organizes an Annual Sports Day every December.",
"Students participate in debates, speech competitions, and science exhibitions.",
"The Annual Function includes cultural performances and prize distribution.",
"The school celebrates Independence Day, Teachers' Day, and other national events.",
"The Robotics Club meets every Saturday after school.",
"The Environmental Club organizes tree plantation campaigns.",
"The Art Club arranges drawing and painting competitions every semester."

]

ids = [f"DOC_{i+1}" for i in range(len(documents))]

if collection.count() == 0:
    collection.add(
        documents=documents,
        ids=ids
    )
    print("Documents Added Successfully!\n")
else:
    print("Database already contains documents.\n")

print("="*60)
print(" SCHOOL KNOWLEDGE ASSISTANT ")
print("="*60)

while True:

    query = input("\nEnter your question (type exit to quit): ")

    if query.lower() == "exit":
        break

    results = collection.query(
        query_texts=[query],
        n_results=3
    )

    print("\nTop 3 Relevant Documents")
    print("-"*60)

    for i in range(len(results["documents"][0])):
        print("ID:", results["ids"][0][i])
        print("Document:", results["documents"][0][i])

        if "distances" in results:
            print("Distance:", results["distances"][0][i])

        print("-"*60)
