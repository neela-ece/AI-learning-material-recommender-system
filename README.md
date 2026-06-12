An AI Learning Material Recommender System is an intelligent platform that recommends suitable learning resources to students based on their interests, learning behavior, skill level, and academic performance. The system uses Artificial Intelligence and Machine Learning algorithms to provide personalized study materials such as videos, notes, tutorials, quizzes, articles, and courses.
The main objective of the system is to help students learn efficiently by reducing the time spent searching for relevant study materials.
# AI Learning Material Recommender System
# Simple Python Project

# Sample learning materials dataset

learning_materials = [
    {
        "title": "Python Basics",
        "category": "Programming",
        "level": "Beginner",
        "link": "https://www.youtube.com/watch?v=_uQrJ0TkZlc"
    },
    {
        "title": "Machine Learning Introduction",
        "category": "AI",
        "level": "Intermediate",
        "link": "https://www.coursera.org/learn/machine-learning"
    },
    {
        "title": "Data Structures in Python",
        "category": "Programming",
        "level": "Intermediate",
        "link": "https://www.geeksforgeeks.org/data-structures/"
    },
    {
        "title": "Deep Learning Course",
        "category": "AI",
        "level": "Advanced",
        "link": "https://www.deeplearning.ai/"
    },
    {
        "title": "HTML and CSS Tutorial",
        "category": "Web Development",
        "level": "Beginner",
        "link": "https://www.w3schools.com/"
    }
]

# Function to recommend materials

def recommend_material(category, level):
    recommendations = []

    for material in learning_materials:
        if material["category"].lower() == category.lower() and \
           material["level"].lower() == level.lower():
            recommendations.append(material)

    return recommendations


# Main Program

print("===== AI Learning Material Recommender System =====")

user_category = input("Enter category (Programming / AI / Web Development): ")
user_level = input("Enter level (Beginner / Intermediate / Advanced): ")

results = recommend_material(user_category, user_level)

print("\nRecommended Learning Materials:\n")

if results:
    for item in results:
        print("Title :", item["title"])
        print("Category :", item["category"])
        print("Level :", item["level"])
        print("Link :", item["link"])
        print("----------------------------------")
else:
    print("No recommendations found.")
