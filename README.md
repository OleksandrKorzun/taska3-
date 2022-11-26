# taska3-
taska = int(input("change A,B or C"))


if taska == "A":
    list = input("Enter text for dictionary: ")
    edited_list = []
    output = ""
    for a in list.split():
        a = a.rstrip(",")
        a = a.rstrip(".")
        a = a.lower()
        if len(a) > 3:
            edited_list.append(a)
    edited_list = sorted(set(edited_list))

    for a in edited_list:
        output += a + "\n"
    print(output)
    
    
elif taska == "B":
    words = []
    a = input("Enter text for top 5 most reapeted words: ")
    words.extend(a.split())
    from collections import Counter
    counts = Counter(words)
    top5 = counts.most_common(5)
    print(top5)
    
    
elif taska == "C":
    def largestWord(s):
        s = sorted(s, key=len)
        print(s[-5:])
    s = input("Enter text for top 5 len words: ")
    l = list(s.split(" "))
    largestWord(l)
