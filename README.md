import tkinter as tk
import keyword
from tkinter import messagebox
from tkinter import ttk
ans={'1':-2,'2':-1,'3':0,'4':1,'5':2}
def i(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    global ie
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(ie=ie-2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(ie=ie-1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(ie=ie+1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(ie=ie+2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)
def e(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    global ie
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(ie=ie+2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(ie=ie+1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(ie=ie-1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(ie=ie-2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)

def n(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    global ns
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(ns=ns-2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(ns=ns-1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(ns=ns+1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(ns=ns+2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)
def s(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(ns=ns+2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(ns=ns+1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(ns=ns-1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(ns=ns-2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)
def t(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    global tf
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(tf=tf-2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(tf=tf-1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(tf=tf+1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(tf=tf+2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)
def f(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    global tf
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(tf=tf+2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(tf=tf+1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(tf=tf-1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(tf=tf-2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)
def p(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    global jp
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(jp=jp-2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(jp=jp-1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(jp=jp+1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(jp=jp+2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)
def j(question):
    for widget in tab1.winfo_children():
        widget.destroy()
    global jp
    ques = tk.Label(tab1, text=question,fg='white',bg='#003366',font=('Arial',12))
    ques.pack(pady=10)
    button_frame = tk.Frame(tab1, bg='#003366')
    button_frame.pack(pady=10)
    op1 = tk.Button(button_frame, text='1',font=('Arial',20) ,bg='#8B0A1A', command=lambda: [globals().update(jp=jp+2), next_question()])
    op1.pack(side=tk.LEFT, padx=5)
    op2 = tk.Button(button_frame, text='2',font=('Arial',20), bg='#FF8080', command=lambda: [globals().update(jp=jp+1), next_question()])
    op2.pack(side=tk.LEFT, padx=5)
    op3 = tk.Button(button_frame, text='3',font=('Arial',20), command=next_question)
    op3.pack(side=tk.LEFT, padx=5)
    op4 = tk.Button(button_frame, text='4',font=('Arial',20) ,bg='#8BC34A', command=lambda: [globals().update(jp=jp-1), next_question()])
    op4.pack(side=tk.LEFT, padx=5)
    op5 = tk.Button(button_frame, text='5',font=('Arial',20) ,bg='#008000', command=lambda: [globals().update(jp=jp-2), next_question()])
    op5.pack(side=tk.LEFT, padx=5)
questions={
    "1.I enjoy being around people and attending social events:":e,
    "2.I tend to focus on the big picture rather than details:":n,
    "3.I make decisions based on logic and objective analysis:":t,
    "4.I enjoy planning and organizing my work and leisure activities:":j,
    "5.I prefer to work independently rather than in a team:":i,
    "6.I tend to trust my instincts and intuition:":n,
    "7.I value harmony and cooperation in my relationships:":f,
    "8.I tend to be more spontaneous and flexible than planned and organized:":p,
}
ques_array=list(questions.keys())
d=open("D:\\python\\descriptions.txt","r")
dptn=d.readlines()
d.close()
def intj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(0,9):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def intp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(10,20):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def entj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(21,29):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def entp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(30,39):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def infj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(40,48):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def infp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(49,57):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def enfj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(58,65):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def enfp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(66,74):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def istj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(75,83):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def isfj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(84,91):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def estj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(92,99):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),end='',fg='white',bg='#003366')
        dn.pack()
def esfj():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(100,107):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def istp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(108,115):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def isfp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(116,123):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def estp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(124,131):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def esfp():
    for widget in tab1.winfo_children():
        widget.destroy()
    for y in range(132,139):
        dn=tk.Label(tab1,text=dptn[y].rstrip('\n'),fg='white',bg='#003366')
        dn.pack()
def next_question():
    global x
    x += 1
    if x < len(ques_array):
        questions[ques_array[x]](ques_array[x])
    else:
        display_results()
def description():
    for widget in tab1.winfo_children():
        widget.destroy()
    if(mbti=='INTJ'):
        intj()
    elif(mbti=='INTP'):
        intp()
    elif(mbti=='ENTJ'):
        entj()
    elif(mbti=='ENTP'):
        entp()
    elif(mbti=='INFJ'):
        infj()
    elif(mbti=='INFP'):
        infp()
    elif(mbti=='ENFJ'):
        enfj()
    elif(mbti=='ENFP'):
        enfp()
    elif(mbti=='ISTJ'):
        istj()
    elif(mbti=='ISFJ'):
        isfj()
    elif(mbti=='ESTJ'):
        estj()
    elif(mbti=='ESFJ'):
        esfj()
    elif(mbti=='ISTP'):
        istp()
    elif(mbti=='ISFP'):
        isfp()
    elif(mbti=='ESTP'):
        estp()
    elif(mbti=='ESFP'):
        esfp()
    reset=tk.Button(tab1,text='Go Back',command=Change2)
    reset.pack(pady=5)
def display_results():
    global perie,perns,pertf,perjp,mbti
    for widget in tab1.winfo_children():
        widget.destroy()
    if ie>0:
        en='I'
        perie=(ie+4)*25/2
    else:
        en='E'
        perie=(4-ie)*25/2
    if ns>0:
        mi='N'
        perns=(ns+4)*25/2
    else:
        mi='S'
        perns=(4-ns)*25/2
    if tf>0:
        na='T'
        pertf=(tf+4)*25/2
    else:
        na='F'
        pertf=(4-tf)*25/2
    if jp>0:
        ta='P'
        perjp=(jp+4)*25/2
    else:
        ta='J'
        perjp=(4-jp)*25/2
    mbti = en + mi + na + ta
    result = tk.Label(tab1, text="Your MBTI type is:-",font=14,fg='white',bg='#003366')
    result.pack(pady=5)
    shre= tk.Label(tab1,text=mbti,font=('Cooper Black',20),fg='white',bg='#003366')
    shre.pack(pady=10)
    percent=tk.Label(
        tab1,
        text=f'''{en}:-{perie}
{mi}:-{perns}
{na}:-{pertf}
{ta}:-{perjp}''',
        fg='white',
        bg='#003366'
    )
    percent.pack(pady=5)
    save=tk.Button(tab1,text='Know more', command=description)
    save.pack(pady=5)
def ttest():
    global x,ie,ns,tf,jp
    ie=0
    ns=0
    tf=0
    jp=0
    x=0
    questions[ques_array[x]](ques_array[x])
    if x < len(ques_array):
        pass
    else:
        display_results()
def instrctn():
    for widget in tab1.winfo_children():
        widget.destroy()
    wlcm=tk.Label(tab1,text="Welcome to MBTI assessment",font=("Cooper Black",20),fg='white',bg='#003366')
    wlcm.pack(pady=5)
    ins=tk.Label(
        tab1,
        text='''Rate the given statements in the range of 1-5.
1 being \'Strongly Disagree\' and 5 being \'Strongly Agree\'.''',
        fg='white',
        bg='#003366'
    )
    ins.pack(pady=15)
    ptest=tk.Button(tab1,text='Proceed',command=ttest)
    ptest.pack(pady=5)
       
def Change():
    global usnm, pw
    usnm = une.get()
    pw = passe.get()
    if usnm != Login[0] or pw != Login[1]:
        messagebox.showerror('Error', 'Username or Password is incorrect!')
    else:
        for widget in tab1.winfo_children():
            widget.destroy()
        wm=tk.Label(tab1,text="MBTI ASSESSMENT",font=('Cooper Black',20,"bold"),fg='#B1B1B1',bg='#003366')
        wm.pack(pady=5)
        wlm=tk.Label(tab1,text=f"Welcome {usnm}",font=('Cooper Black',20),fg='#B1B1B1',bg='#003366')
        wlm.pack()
        test = tk.Button(tab1, text='Take test', command=instrctn)
        test.pack(pady=10)
        history=tk.Button(tab1,text='History')
        history.pack(pady=5)
        profile=tk.Button(tab1,text='Profile')
        profile.pack(pady=10)
def Change2():
    for widget in tab1.winfo_children():
            widget.destroy()
    wm=tk.Label(tab1,text="MBTI ASSESSMENT",font=('Cooper Black',20,"bold"),fg='#B1B1B1',bg='#003366')
    wm.pack(pady=5)
    wlm=tk.Label(tab1,text=f"Welcome {usnm}",font=('Cooper Black',20),fg='#B1B1B1',bg='#003366')
    wlm.pack()
    test = tk.Button(tab1, text='Take test', command=instrctn)
    test.pack(pady=10)
    history=tk.Button(tab1,text='History')
    history.pack(pady=5)
    profile=tk.Button(tab1,text='Profile')
    profile.pack(pady=10)
strength=open("D:\\python\\Strengths.txt","r")
stn=strength.readlines()
weakness=open("D:\\python\\Weakness.txt","r")
wkn=weakness.readlines()
career=open("D:\\python\\Career.txt","r")
crr=career.readlines()
def intj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="INTJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Architect',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(0,3):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(0,3):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(0,5):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def intp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="INTP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Logician',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(4,7):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(4,7):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(6,11):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))        
def entj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ENTJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Commander',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(8,11):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(8,11):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(12,17):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def entp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ENTP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Debater',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(12,15):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(12,15):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(18,23):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def infj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="INFJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Advocate',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(16,19):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(16,19):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(24,29):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def infp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="INFP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Mediator',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(20,23):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(20,23):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(30,35):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def enfj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ENFJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Protagonist',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(24,27):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(24,27):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(36,41):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def enfp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ENFP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Campaigner',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(28,31):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(28,31):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(42,47):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def istj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ISTJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Logistician',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(32,35):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(32,35):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(48,53):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def isfj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ISFJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Defender',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(36,39):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(36,39):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(54,59):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def estj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ESTJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Executive',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(40,43):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(40,43):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(60,65):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def esfj_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ESFJ",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Consul',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(44,47):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(44,47):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(66,71):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def istp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ISTP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Virtuoso',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(48,51):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(48,51):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(72,77):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def isfp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ISFP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Adventurer',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(52,55):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(52,55):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(78,83):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def estp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ESTP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Entrepreneur',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(56,59):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(56,59):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(84,89):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
def esfp_brief():
    for widget in tab3.winfo_children():
        widget.destroy()
    framed = tk.Frame(tab3)
    framed.pack(fill="both", expand=True)
    scrollbard = tk.Scrollbar(framed)
    scrollbard.pack(side="right", fill="y")
    canvasd = tk.Canvas(framed, yscrollcommand=scrollbard.set)
    canvasd.pack(side="left", fill="both", expand=True)
    scrollbard.config(command=canvasd.yview)
    inner_framed = tk.Frame(canvasd,bg='#003366')
    canvasd.create_window((0, 0), window=inner_framed, anchor='nw')
    typet= tk.Label(inner_framed, text="ESFP",fg='#B1B1B1',bg='#003366',font=('Cooper Black',20))
    typet.pack(padx=100)
    sp1=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp1.pack()
    knas=tk.Label(inner_framed,text='Known as',fg='white',bg='#003366',font=('Cooper Black',14))
    knas.pack()
    namet=tk.Label(inner_framed,text='Entertainer',fg='#B1B1B1',bg='#003366',font=('Cooper Black',14))
    namet.pack()
    sp2=tk.Label(inner_framed,text='--------------------------',fg='white',bg='#003366')
    sp2.pack()
    strengtht= tk.Label(inner_framed, text="Strengths",fg='white',bg='#003366',font=('Cooper Black',14))
    strengtht.pack(padx=100,pady=10)
    for i in range(60,63):
        strengthd = tk.Label(inner_framed, text=stn[i].rstrip('\n'),fg='white',bg='#003366')
        strengthd.pack()
    weaknesst= tk.Label(inner_framed, text="Weakness",fg='white',bg='#003366',font=('Cooper Black',14))
    weaknesst.pack(padx=100,pady=10)
    for i in range(60,63):
        weaknessd = tk.Label(inner_framed, text=wkn[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    careert=tk.Label(inner_framed,text="Potential Career Paths",fg='white',bg='#003366',font=('Cooper Black',14))
    careert.pack(pady=10)
    for i in range(90,95):
        weaknessd = tk.Label(inner_framed, text=crr[i].rstrip('\n'),fg='white',bg='#003366')
        weaknessd.pack()
    back3=tk.Button(inner_framed,text="Go Back",command=tab3_management)
    back3.pack(pady=10)
    inner_framed.update_idletasks()
    canvasd.config(scrollregion=canvas.bbox("all"))
strength.close()
weakness.close()
career.close()
def tab3_management():
    for widget in tab3.winfo_children():
        widget.destroy()
    frame3 = tk.Frame(tab3)
    frame3.pack(fill="both", expand=True)
    scrollbar3 = tk.Scrollbar(frame3)
    scrollbar3.pack(side="right", fill="y")
    canvas3 = tk.Canvas(frame3, yscrollcommand=scrollbar3.set)
    canvas3.pack(side="left", fill="both", expand=True)
    scrollbar3.config(command=canvas3.yview)
    inner_frame3 = tk.Frame(canvas3,bg='#003366')
    canvas3.create_window((0, 0), window=inner_frame3, anchor='nw')
    Show=tk.Label(inner_frame3,text="16 Personality type",font=("Cooper Black",15,"bold"),fg='white',bg='#003366')
    Show.pack(fill="x",padx=50)
    analyst=tk.Label(inner_frame3,text='Analysts',font=("Cooper Black",14,"bold"),fg='purple',bg='#003366')
    analyst.pack()
    row_frame1=tk.Frame(inner_frame3,bg='#003366')
    row_frame1.pack(fill="x",pady=10)
    intjl = tk.Label(row_frame1, text="INTJ",font=("Cooper Black",12,"bold"),fg='#D8BFD8',bg='#003366')
    intjl.pack(side=tk.LEFT,padx=5)
    intjb=tk.Button(row_frame1,text="INTJ Insights",bg='#D8BFD8',command=intj_brief)
    intjb.pack(side=tk.RIGHT,padx=50)
    row_frame2=tk.Frame(inner_frame3,bg='#003366')
    row_frame2.pack(fill="x",pady=10)
    intpl = tk.Label(row_frame2, text="INTP",font=("Cooper Black",12,"bold"),fg='#D8BFD8',bg='#003366')
    intpl.pack(side=tk.LEFT,padx=5)
    intpb=tk.Button(row_frame2,text="INTP Insights",bg='#D8BFD8',command=intp_brief)
    intpb.pack(side=tk.RIGHT,padx=50)
    row_frame3=tk.Frame(inner_frame3,bg='#003366')
    row_frame3.pack(fill="x",pady=10)
    entjl = tk.Label(row_frame3, text="ENTJ",font=("Cooper Black",12,"bold"),fg='#D8BFD8',bg='#003366')
    entjl.pack(side=tk.LEFT,padx=5)
    entjb=tk.Button(row_frame3,text="ENTJ Insights",bg='#D8BFD8',command=entj_brief)
    entjb.pack(side=tk.RIGHT,padx=50)
    row_frame4=tk.Frame(inner_frame3,bg='#003366')
    row_frame4.pack(fill="x",pady=10)
    entpl = tk.Label(row_frame4, text="ENTP",font=("Cooper Black",12,"bold"),fg='#D8BFD8',bg='#003366')
    entpl.pack(side=tk.LEFT,padx=5)
    entpb=tk.Button(row_frame4,text="ENTP Insights",bg='#D8BFD8',command=entp_brief)
    entpb.pack(side=tk.RIGHT,padx=50)
    diplomats=tk.Label(inner_frame3,text='Diplomats',font=("Cooper Black",14,"bold"),fg='green',bg='#003366')
    diplomats.pack()
    row_frame5=tk.Frame(inner_frame3,bg='#003366')
    row_frame5.pack(fill="x",pady=10)
    infjl = tk.Label(row_frame5, text="INFJ",font=("Cooper Black",12,"bold"),fg='#90EE90',bg='#003366')
    infjl.pack(side=tk.LEFT,padx=5)
    infjb=tk.Button(row_frame5,text="INFJ Insights",bg='#90EE90',command=infj_brief)
    infjb.pack(side=tk.RIGHT,padx=50)
    row_frame6=tk.Frame(inner_frame3,bg='#003366')
    row_frame6.pack(fill="x",pady=10)
    infpl = tk.Label(row_frame6, text="INFP",font=("Cooper Black",12,"bold"),fg='#90EE90',bg='#003366')
    infpl.pack(side=tk.LEFT,padx=5)
    infpb=tk.Button(row_frame6,text="INFP Insights",bg='#90EE90',command=infp_brief)
    infpb.pack(side=tk.RIGHT,padx=50)
    row_frame7=tk.Frame(inner_frame3,bg='#003366')
    row_frame7.pack(fill="x",pady=10)
    enfjl = tk.Label(row_frame7, text="ENFJ",font=("Cooper Black",12,"bold"),fg='#90EE90',bg='#003366')
    enfjl.pack(side=tk.LEFT,padx=5)
    enfjb=tk.Button(row_frame7,text="ENFJ Insights",bg='#90EE90',command=enfj_brief)
    enfjb.pack(side=tk.RIGHT,padx=50)
    row_frame8=tk.Frame(inner_frame3,bg='#003366')
    row_frame8.pack(fill="x",pady=10)
    enfpl = tk.Label(row_frame8, text="ENFP",font=("Cooper Black",12,"bold"),fg='#90EE90',bg='#003366')
    enfpl.pack(side=tk.LEFT,padx=5)
    enfpb=tk.Button(row_frame8,text="ENFP Insights",bg='#90EE90',command=enfp_brief)
    enfpb.pack(side=tk.RIGHT,padx=50)
    sentinels=tk.Label(inner_frame3,text='Sentinels',font=("Cooper Black",14,"bold"),fg='#00BFFF',bg='#003366')
    sentinels.pack()
    row_frame9=tk.Frame(inner_frame3,bg='#003366')
    row_frame9.pack(fill="x",pady=10)
    istjl = tk.Label(row_frame9, text="ISTJ",font=("Cooper Black",12,"bold"),fg='#87CEEB',bg='#003366')
    istjl.pack(side=tk.LEFT,padx=5)
    istjb=tk.Button(row_frame9,text="ISTJ Insights",bg='#87CEEB',command=istj_brief)
    istjb.pack(side=tk.RIGHT,padx=50)
    row_frame10=tk.Frame(inner_frame3,bg='#003366')
    row_frame10.pack(fill="x",pady=10)
    isfjl = tk.Label(row_frame10, text="ISFJ",font=("Cooper Black",12,"bold"),fg='#87CEEB',bg='#003366')
    isfjl.pack(side=tk.LEFT,padx=5)
    isfjb=tk.Button(row_frame10,text="ISFJ Insights",bg='#87CEEB',command=isfj_brief)
    isfjb.pack(side=tk.RIGHT,padx=50)
    row_frame11=tk.Frame(inner_frame3,bg='#003366')
    row_frame11.pack(fill="x",pady=10)
    estjl = tk.Label(row_frame11, text="ESTJ",font=("Cooper Black",12,"bold"),fg='#87CEEB',bg='#003366')
    estjl.pack(side=tk.LEFT,padx=5)
    estjb=tk.Button(row_frame11,text="ESTJ Insights",bg='#87CEEB',command=estj_brief)
    estjb.pack(side=tk.RIGHT,padx=50)
    row_frame12=tk.Frame(inner_frame3,bg='#003366')
    row_frame12.pack(fill="x",pady=10)
    esfjl = tk.Label(row_frame12, text="ESFJ",font=("Cooper Black",12,"bold"),fg='#87CEEB',bg='#003366')
    esfjl.pack(side=tk.LEFT,padx=5)
    esfjb=tk.Button(row_frame12,text="ESFJ Insights",bg='#87CEEB',command=esfj_brief)
    esfjb.pack(side=tk.RIGHT,padx=50)
    esfjb.pack(side=tk.RIGHT,padx=50)
    explorers=tk.Label(inner_frame3,text='Explorers',font=("Cooper Black",14,"bold"),fg='yellow',bg='#003366')
    explorers.pack()
    row_frame13=tk.Frame(inner_frame3,bg='#003366')
    row_frame13.pack(fill="x",pady=10)
    istpl = tk.Label(row_frame13, text="ISTP",font=("Cooper Black",12,"bold"),fg='#F7DC6F',bg='#003366')
    istpl.pack(side=tk.LEFT,padx=5)
    istpb=tk.Button(row_frame13,text="ISTP Insights",bg='#F7DC6F',command=istp_brief)
    istpb.pack(side=tk.RIGHT,padx=50)
    row_frame14=tk.Frame(inner_frame3,bg='#003366')
    row_frame14.pack(fill="x",pady=10)
    isfpl = tk.Label(row_frame14, text="ISFP",font=("Cooper Black",12,"bold"),fg='#F7DC6F',bg='#003366')
    isfpl.pack(side=tk.LEFT,padx=5)
    isfpb=tk.Button(row_frame14,text="ISFP Insights",bg='#F7DC6F',command=isfp_brief)
    isfpb.pack(side=tk.RIGHT,padx=50)
    row_frame15=tk.Frame(inner_frame3,bg='#003366')
    row_frame15.pack(fill="x",pady=10)
    estpl = tk.Label(row_frame15, text="ESTP",font=("Cooper Black",12,"bold"),fg='#F7DC6F',bg='#003366')
    estpl.pack(side=tk.LEFT,padx=5)
    estpb=tk.Button(row_frame15,text="ESTP Insights",bg='#F7DC6F',command=estp_brief)
    estpb.pack(side=tk.RIGHT,padx=50)
    row_frame16=tk.Frame(inner_frame3,bg='#003366')
    row_frame16.pack(fill="x",pady=10)
    esfpl = tk.Label(row_frame16, text="ESFP",font=("Cooper Black",12,"bold"),fg='#F7DC6F',bg='#003366')
    esfpl.pack(side=tk.LEFT,padx=5)
    esfpb=tk.Button(row_frame16,text="ESFP Insights",bg='#F7DC6F',command=esfp_brief)
    esfpb.pack(side=tk.RIGHT,padx=50)
    inner_frame3.update_idletasks()
    canvas3.config(scrollregion=canvas3.bbox("all"))

root=tk.Tk()
root.title('MBTI assessment')
notebook = ttk.Notebook(root)
notebook.pack()
tab1 = tk.Frame(notebook,bg="#003366")
tab2 = tk.Frame(notebook)
tab3 = tk.Frame(notebook)
notebook.add(tab1, text='Home')
notebook.add(tab2, text='What\'s MBTI')
notebook.add(tab3, text='Personality Types')
Login=['Roomi','123']
root.geometry('600x350')
title=tk.Label(tab1,text='Login',font=('Cooper Black',24),fg='white',bg='#003366')
title.pack(pady=5)
un=tk.Label(tab1,text='Username:',fg='white',bg='#003366')
un.pack(pady=10)
une=tk.Entry(tab1)
une.pack()
passl=tk.Label(tab1,text='Password:',fg='white',bg='#003366')
passl.pack(pady=10)
passe=tk.Entry(tab1)
passe.pack()
proceed=tk.Button(tab1,text='Save',command=Change,bg='#F7F7F7')
proceed.pack(pady=5)
m=open("D:\\python\\mechanism.txt","r")
frame = tk.Frame(tab2)
frame.pack(fill="both", expand=True)
scrollbar = tk.Scrollbar(frame)
scrollbar.pack(side="right", fill="y")
canvas = tk.Canvas(frame, yscrollcommand=scrollbar.set)
canvas.pack(side="left", fill="both", expand=True)
scrollbar.config(command=canvas.yview)
inner_frame = tk.Frame(canvas,bg='#003366')
canvas.create_window((0, 0), window=inner_frame, anchor='nw')
uds=tk.Label(inner_frame,text='UNDERSTANDING',font=('Cooper Black',20),fg='white',bg='#003366')
uds.pack(pady=5)
mbt=tk.Label(inner_frame,text='MBTI',font=('Cooper Black',20),fg='white',bg='#003366')
mbt.pack()
label = tk.Label(inner_frame, text=m.read(),fg='white',bg='#003366')
label.pack(pady=10)
inner_frame.update_idletasks()
canvas.config(scrollregion=canvas.bbox("all"))
m.close()
tab3_management()

root.mainloop()

