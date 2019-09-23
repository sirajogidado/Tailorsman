# Tailorsman

Tailorsman will be a nigerian software app that will enable customers to 
create and design their own tailored suits using their measurements. 
this will enable alot of users to know their sizes before going to the tailor 
for their various suits.


import tkinter as tk

colours = ['red','green','orange','white','yellow','blue']

r = 0
for c in colours:
    tk.Label(text=c, relief=tk.RIDGE, width=15).grid(row=r,column=0)
    tk.Entry(bg=c, relief=tk.SUNKEN, width=10).grid(row=r,column=1)
    r = r + 1

def translate(phrase):
    translation = ""
    for letter in phrase:
        if letter in 'AEIOUaeiou':
            translation = translation + 'x'
        else:
            translation = translation + letter
    return translation

print(translate(input('Enter a phrase: ')))

tk.mainloop()
