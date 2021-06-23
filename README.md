# guess_who
NAMES = ("Michael", "James", "Oscar", "Fred", "Steve", "Ace", "Bill", "Marcus", "Brian", "Jeremy",
         "Eliza", "Faith", "Sally", "Maria", "Jacqueline", "Cheri", "Ashley", "Emily", "Bianca", "Alice")
GENDERS = ("male", "female")
EYE_COLORS = ("blue", "green", "brown")
HAIR_COLORS = ("black", "red", "blonde", "grey", "brown")
RACE = ("white", "black", "hispanic", "asian")
FACIAL_HAIR = ("none", "mustache", "beard")
JEWELRY = ("necklace", "ear rings", "glasses", "none")


question_bank = [" "]

def question_generator():

    for gender in GENDERS:
        question_bank.append(f"Are you a {gender}?")
    for eye_color in EYE_COLORS:
        question_bank.append(f"Does your person have {eye_color} eyes?")
    for hair_color in HAIR_COLORS:
        question_bank.append(f"Does your person have {hair_color} hair?")
    for race in RACE:
        question_bank.append(f"Is your person {race}?")
    for style in FACIAL_HAIR:
        if style == "none":
            question_bank.append(f"Was your person skipped when God handed out the facial hair genes?")
        else:
            question_bank.append(f"Does your person have a {style}")
    for item in JEWELRY:
        if item == "none":
            question_bank.append(f"Is your person NOT wearing glasses or jewelry?")
        else:
            question_bank.append(f"Is your person wearing {item}")
    for name in NAMES:
        question_bank.append(f"Is your person {name}?")

    question_num = 1
    for question in question_bank:
        if question != " ":
            print(f"{question_num}. {question}")
            question_num += 1



question_generator()


people_dict ={
    "Michael":
        {"gender": "male", "eye_color": "blue", "hair_color": "blonde", "race": "white", "facial_hair": "none", "jewelry": "glasses"},
    "James":
        {"gender": "male", "eye_color": "green", "hair_color": "black", "race": "black", "facial_hair": "mustache", "jewelry": "none"},
    "Oscar":
        {"gender": "male", "eye_color": "brown", "hair_color": "brown", "race": "hispanic", "facial_hair": "beard", "jewelry": "none"},
    "Fred":
        {"gender": "male", "eye_color": "blue", "hair_color": "black", "race": "asian", "facial_hair": "none", "jewelry": "none"},
    "Steve":
        {"gender": "male", "eye_color": "green", "hair_color": "grey", "race": "white", "facial_hair": "mustache", "jewelry": "none"},
    "Ace":
        {"gender": "male", "eye_color": "brown", "hair_color": "black", "race": "black", "facial_hair": "beard", "jewelry": "glasses"},
    "Bill":
        {"gender": "male", "eye_color": "blue", "hair_color": "red", "race": "white", "facial_hair": "none", "jewelry": "none"},
    "Juan":
        {"gender": "male", "eye_color": "green", "hair_color": "brown", "race": "hispanic", "facial_hair": "mustache", "jewelry": "none"},
    "Brian":
        {"gender": "male", "eye_color": "brown", "hair_color": "blonde", "race": "black", "facial_hair": "beard", "jewelry": "none"},
    "Bruce":
        {"gender": "male", "eye_color": "brown", "hair_color": "grey", "race": "asian", "facial_hair": "none", "jewelry": "glasses"},
    "Eliza":
        {"gender": "female", "eye_color": "brown", "hair_color": "grey", "race": "hispanic", "facial_hair": "none", "jewelry": "glasses"},
    "Faith":
        {"gender": "female", "eye_color": "brown", "hair_color": "black", "race": "black", "facial_hair": "none", "jewelry": "necklace"},
    "Sally":
        {"gender": "female", "eye_color": "blue", "hair_color": "blonde", "race": "white", "facial_hair": "none", "jewelry": "ear rings"},
    "Maria":
        {"gender": "female", "eye_color": "brown", "hair_color": "brown", "race": "hispanic", "facial_hair": "none", "jewelry": "none"},
    "Linnie":
        {"gender": "female", "eye_color": "blue", "hair_color": "brown", "race": "asian", "facial_hair": "none", "jewelry": "glasses"},
    "Cheri":
        {"gender": "female", "eye_color": "green", "hair_color": "blonde", "race": "white", "facial_hair": "none", "jewelry": "ear rings"},
    "Ashley":
        {"gender": "female", "eye_color": "brown", "hair_color": "black", "race": "black", "facial_hair": "none", "jewelry": "necklace"},
    "Emily":
        {"gender": "female", "eye_color": "blue", "hair_color": "black", "race": "asian", "facial_hair": "none", "jewelry": "glasses"},
    "Bianca":
        {"gender": "female", "eye_color": "green", "hair_color": "grey", "race": "black", "facial_hair": "none", "jewelry": "none"},
    "Alice":
        {"gender": "female", "eye_color": "blue", "hair_color": "red", "race": "white", "facial_hair": "none", "jewelry": "glasses"}
}

for key, value in people_dict.items():
    if  people_dict[key]["jewelry"] == "glasses":
        print(key)




