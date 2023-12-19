import tkinter as tk
import random


def urben():
    def lo():
        global c, c2, nol, nol_sum
        if c == 2:
            a = random.randint(1, 10)
            s = 0
            for i in range(0, len(list)):
                if a == list[i]:
                    s += 1
            for i in range(0, 10):
                if 5 == i:
                    c2 += 1
            if c2 == 0:
                btn4.config
            if s > 0:
                lo()
            if a == 1 and s == 0:
                btn.config(text="O")
                list.append(1)
            if a == 2 and s == 0:
                btn1.config(text="O")
                list.append(2)
            if a == 3 and s == 0:
                btn2.config(text="O")
                list.append(3)
            if a == 4 and s == 0:
                btn3.config(text="O")
                list.append(4)
            if a == 5 and s == 0:
                btn4.config(text="O")
                list.append(5)
            if a == 6 and s == 0:
                btn5.config(text="O")
                list.append(6)
            if a == 7 and s == 0:
                btn6.config(text="O")
                list.append(7)
            if a == 8 and s == 0:
                btn7.config(text="O")
                list.append(8)
            if a == 9 and s == 0:
                btn8.config(text="O")
                list.append(9)
        if c == 1:
            a = random.randint(1, 10)
            s = 0
            for i in range(0, len(list)):
                if a == list[i]:
                    s += 1
            if s > 0:
                lo()
            if a == 1 and s == 0 and (kres + a) % 3 == 0:
                btn.config(text="O")
                list.append(1)
            if a == 2 and s == 0 and (kres + a) % 3 == 0:
                btn1.config(text="O")
                list.append(2)
            if a == 3 and s == 0 and (kres + a) % 3 == 0:
                btn2.config(text="O")
                list.append(3)
            if a == 4 and s == 0 and (kres + a) % 3 == 0:
                btn3.config(text="O")
                list.append(4)
            if a == 5 and s == 0 and (kres + a) % 3 == 0:
                btn4.config(text="O")
                list.append(5)
            if a == 6 and s == 0 and (kres + a) % 3 == 0:
                btn5.config(text="O")
                list.append(6)
            if a == 7 and s == 0 and (kres + a) % 3 == 0:
                btn6.config(text="O")
                list.append(7)
            if a == 8 and s == 0 and (kres + a) % 3 == 0:
                btn7.config(text="O")
                list.append(8)
            if a == 9 and s == 0 and (kres + a) % 3 == 0:
                btn8.config(text="O")
                list.append(9)
        elif c == 0:
            a = random.randint(1, 10)
            s = 0
            for i in range(0, len(list)):
                if a == list[i]:
                    s = +1
            if s > 0:
                lo()
            if a == 1 and s == 0:
                btn.config(text="O")
                list.append(1)
            if a == 2 and s == 0:
                btn1.config(text="O")
                list.append(2)
            if a == 3 and s == 0:
                btn2.config(text="O")
                list.append(3)
            if a == 4 and s == 0:
                btn3.config(text="O")
                list.append(4)
            if a == 5 and s == 0:
                btn4.config(text="O")
                list.append(5)
            if a == 6 and s == 0:
                btn5.config(text="O")
                list.append(6)
            if a == 7 and s == 0:
                btn6.config(text="O")
                list.append(7)
            if a == 8 and s == 0:
                btn7.config(text="O")
                list.append(8)
            if a == 9 and s == 0:
                btn8.config(text="O")
                list.append(9)

    def win():
        global c2
        for i in range(0, len(list) - 1):
            if list[i] - list[i + 1] == 1 or list[i] - list[i + 1] == -1:
                c2 += 1
        if c2 == 0:
            win = tk.Button(root, text=" WIN", font=("Arial", 20), width=12, height=5,
                            command=lambda row=100, col=100: win1(row, col))
            win.grid(row=300, column=300)

    def win1(row, col):
        global c, list
        if c < 3:
            c += 1
            list.clear()
            urben()

    def s(row, col):
        global count, kres_sum, nol_sum, kres, nol
        lo()
        count += 1
        btn.config(text="X")
        list.append(int(1))
        kres += 1
        print(kres)
        kres_sum += 1
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s1(row, col):
        global count, kres_sum, nol_sum, kres, nol
        count += 1
        list.append(2)
        btn1.config(text="X")
        kres += 2
        kres_sum += 1
        lo()
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s2(row, col):
        global count, kres_sum, nol_sum, kres, nol
        count += 1
        list.append(3)
        btn2.config(text="X")
        kres += 3
        kres_sum += 1
        lo()
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s3(row, col):
        global count, kres_sum, nol_sum, kres, nol
        count += 1
        btn3.config(text="X")
        list.append(4)
        kres += 4
        kres_sum += 1
        lo()
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s4(row, col):
        global count, kres_sum, nol_sum, kres, nol
        lo()
        count += 1
        btn4.config(text="X")
        list.append(5)
        kres += 5
        kres_sum += 1
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s5(row, col):
        global count, kres_sum, nol_sum, kres, nol
        count += 1
        btn5.config(text="X")
        list.append(6)
        kres += 6
        print(kres)
        kres_sum += 1
        lo()
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s6(row, col):
        global count, kres_sum, nol_sum, kres, nol
        count += 1
        btn6.config(text="X")
        list.append(7)
        kres += 7
        kres_sum += 1
        lo()
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s7(row, col):
        global count, kres_sum, nol_sum, kres, nol
        count += 1
        btn7.config(text="X")
        list.append(8)
        kres += 8
        print(kres)
        kres_sum += 1
        lo()
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    def s8(row, col):
        global count, kres_sum, nol_sum, kres, nol
        lo()
        count += 1
        btn8.config(text="X")
        list.append(9)
        kres += 9
        print(kres)
        kres_sum += 1
        if kres_sum == 4:
            for i in range(0, len(list)):
                if (kres - list[i]) % 3 == 0:
                    kres -= list[i]
        print(kres)
        if kres % 3 == 0 and kres_sum >= 3:
            win()
            kres = 0
            kres_sum = 0

    buttons = [[None for _ in range(3)] for _ in range(3)]

    btn = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                    command=lambda row=100, col=100: s(row, col))
    btn.grid(row=100, column=100)

    btn1 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s1(row, col))
    btn1.grid(row=100, column=300)

    btn2 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s2(row, col))
    btn2.grid(row=100, column=500)

    btn3 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s3(row, col))
    btn3.grid(row=300, column=100)

    btn4 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s4(row, col))
    btn4.grid(row=300, column=300)

    btn5 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s5(row, col))
    btn5.grid(row=300, column=500)

    btn6 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s6(row, col))
    btn6.grid(row=500, column=100)

    btn7 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s7(row, col))
    btn7.grid(row=500, column=300)

    btn8 = tk.Button(root, text=" ", font=("Arial", 20), width=12, height=5,
                     command=lambda row=100, col=100: s8(row, col))
    btn8.grid(row=500, column=500)


root = tk.Tk()
root.title("крестики нолики")
root.geometry("605x552")
list = []
kres = 0
c = 0
c2 = 0
nol = 0
kres_sum = 0
nol_sum = 0
ur = 0
count = 0
urben()
root.mainloop()
