# 📚 Discrete Mathematics (ডিসক্রিট ম্যাথমেটিক্স) — Exam Preparation Guide (বাংলায়)

---

# 🔷 পার্ট ১: Relation (সম্পর্ক) এর Properties (বৈশিষ্ট্য)

Relations-এর ৫টি গুরুত্বপূর্ণ বৈশিষ্ট্য আছে। নিচে প্রতিটি সহজ বাংলায় ব্যাখ্যা করা হলো:

---

## 1. Reflexive (প্রতিবর্তী / রিফ্লেক্সিভ)

> **সংজ্ঞা:** একটি Relation R, সেট A-এর উপর **reflexive** হবে যদি সেট A-এর প্রতিটি element (উপাদান) নিজের সাথে সম্পর্কিত হয়।

**গাণিতিক শর্ত:** ∀a ∈ A → (a, a) ∈ R

**সহজ ভাষায়:** সেটের প্রতিটি element-এর জন্য নিজের সাথে নিজের relation থাকতে হবে।

**উদাহরণ:** A = {a, b, c}

```
✅ Reflexive:    R = {<a,a>, <b,b>, <c,c>, <a,b>}
                  (a,a), (b,b), (c,c) সব আছে → reflexive

❌ NOT Reflexive: R = {<a,a>, <b,b>, <a,b>}
                  (c,c) নেই → reflexive না
```

**পরীক্ষার টেকনিক:**
- Diagonal elements (a,a), (b,b), (c,c) — সবগুলো আছে কিনা দেখো
- একটাও diagonal pair missing থাকলে reflexive না

---

## 2. Irreflexive (অপ্রতিবর্তী / ইররিফ্লেক্সিভ)

> **সংজ্ঞা:** একটি Relation R, সেট A-এর উপর **irreflexive** হবে যদি সেট A-এর কোনো element নিজের সাথে সম্পর্কিত না হয়।

**গাণিতিক শর্ত:** ∀a ∈ A → (a, a) ∉ R

**সহজ ভাষায়:** কেউ নিজের সাথে সম্পর্কিত না।

**উদাহরণ:** A = {a, b, c}

```
✅ Irreflexive:   R = {<a,b>, <b,c>, <c,a>}
                   (a,a), (b,b), (c,c) একটাও নেই → irreflexive

❌ NOT Irreflexive: R = {<a,b>, <a,a>, <b,c>}
                   (a,a) আছে → irreflexive না
```

**মনে রাখার টেকনিক:**
- Reflexive: সব diagonal pair আছে
- Irreflexive: একটাও diagonal pair নেই
- কোনোটা না কোনোটা: কিছু diagonal আছে, কিছু নেই

---

## 3. Symmetric (প্রতিসম / সিমেট্রিক)

> **সংজ্ঞা:** একটি Relation R, **symmetric** হবে যদি (a,b) ∈ R হলে (b,a) ∈ R হয়।

**গাণিতিক শর্ত:** যদি (a, b) ∈ R → (b, a) ∈ R

**সহজ ভাষায়:** সম্পর্ক দুই দিকে চলে — যদি a, b-এর সাথে সম্পর্কিত হয়, তাহলে b, a-এর সাথেও সম্পর্কিত হবে।

**উদাহরণ:** A = {a, b, c}

```
✅ Symmetric:      R = {<a,b>, <b,a>, <c,c>}
                    <a,b> এর জন্য <b,a> আছে, <c,c> নিজেই symmetric

❌ NOT Symmetric:  R = {<a,b>, <b,c>, <c,c>}
                    <a,b> আছে কিন্তু <b,a> নেই → symmetric না
```

**পরীক্ষার টেকনিক:** 
- প্রতিটি pair (x,y)-এর জন্য (y,x) আছে কিনা check করো

---

## 4. Anti-symmetric (প্রতি-প্রতিসম / অ্যান্টি-সিমেট্রিক)

> **সংজ্ঞা:** একটি Relation R, **anti-symmetric** হবে যদি (a,b) ∈ R এবং (b,a) ∈ R হলে a = b হয়।

**গাণিতিক শর্ত:** যদি (a, b) ∈ R ∧ (b, a) ∈ R → a = b

**সহজ ভাষায়:** দু-দিকে relation থাকলে তারা একই element হতে হবে। অর্থাৎ (a,b) এবং (b,a) একসাথে থাকতে পারবে না, যদি না a = b হয়।

**উদাহরণ:** A = {a, b, c}

```
✅ Anti-symmetric:    R = {<a,b>, <b,c>, <a,a>, <b,b>}
                       <a,b> আছে কিন্তু <b,a> নেই → OK
                       <b,c> আছে কিন্তু <c,b> নেই → OK
                       <a,a>, <b,b> নিজের সাথে → OK

❌ NOT Anti-symmetric: R = {<a,b>, <b,a>, <c,c>}
                       <a,b> এবং <b,a> দুটোই আছে, কিন্তু a ≠ b → anti-symmetric না
```

**Symmetric vs Anti-symmetric পার্থক্য:**

| Symmetric | Anti-symmetric |
|-----------|---------------|
| (a,b) → (b,a) থাকতে হবে | (a,b) এবং (b,a) একসাথে থাকতে পারবে না |
| দুই দিকে relation | এক দিকে (নিজে ছাড়া) |

---

## 5. Transitive (স�্ক্রামক / ট্রানজিটিভ)

> **সংজ্ঞা:** একটি Relation R, **transitive** হবে যদি (a,b) ∈ R এবং (b,c) ∈ R হলে (a,c) ∈ R হয়।

**গাণিতিক শর্ত:** যদি (a, b) ∈ R ∧ (b, c) ∈ R → (a, c) ∈ R

**সহজ ভাষায়:** chain তৈরি হলে সরাসরি connection-ও থাকতে হবে।

**উদাহরণ:** A = {1, 2, 3}

```
✅ Transitive:     R = {<1,2>, <2,3>, <1,3>, <1,1>}
                    <1,2> + <2,3> → <1,3> আছে ✓
                    অন্যসব chain check → OK

❌ NOT Transitive: R = {<1,2>, <2,3>}
                    <1,2> + <2,3> → <1,3> নেই → transitive না
```

**পরীক্ষার টেকনিক:** সব সম্ভাব্য pair ধরে transitive check করা লাগবে। সবগুলো chain check করতে হবে।

**Transitive check করার সহজ নিয়ম (Warshall's Algorithm approach):**
- যদি (a,b) এবং (b,c) থাকে, (a,c) আছে কিনা দেখো
- না থাকলেই transitive না

---

## 6. Equivalence Relation (সমতুল্যতা সম্পর্ক)

> কোনো Relation **equivalence relation** হবে যদি তা **Reflexive + Symmetric + Transitive** তিনটিই হয়।

```
Equivalence Relation = Reflexive + Symmetric + Transitive
```

**Q20 এর উদাহরণ:** A = {a, b, c}, R = {<a,a>, <b,b>, <c,c>, <a,b>}
- Reflexive? → (a,a), (b,b), (c,c) সব আছে → ✅
- Symmetric? → <a,b> আছে কিন্তু <b,a> নেই → ❌
- ∴ Equivalence relation না

---

# 🔷 পার্ট ২: Partial Order (আংশিক ক্রম) এবং Hasse Diagram

## Partial Order Relation (আংশিক ক্রম সম্পর্ক)

কোনো Relation **Partial Order** হবে যদি তা:
```
Partial Order = Reflexive + Anti-symmetric + Transitive
```

## Hasse Diagram (হাসে ডায়াগ্রাম)

Hasse diagram হলো partial order relation-এর graphical representation।

**Hasse Diagram আঁকার নিয়ম:**
1. Reflexive loops বাদ দাও (সব node-এ নিজের loop আছে ধরে নেওয়া হয়)
2. Transitive edges বাদ দাও (chain থাকলে শেষের direct edge বাদ দাও)
3. ছোট element নিচে, বড় element উপরে বসাও (arrow head বাদ)

---

## Maximal এবং Minimal Element

> Partial Order Set (poset) এ:
> - **Maximal Element:** যার চেয়ে বড় কোনো element নেই
> - **Minimal Element:** যার চেয়ে ছোট কোনো element নেই
> - **Greatest Element (সর্বোচ্চ):** যেটা সকলের চেয়ে বড় (সবার উপরে)
> - **Least Element (সর্বনিম্ন):** যেটা সকলের চেয়ে ছোট (সবার নিচে)

**Hasse Diagram-এ চেনার উপায়:**

```
         d        ← d হলো maximal (উপরে কেউ নেই)
        / \
       b   c      ← b, c — মধ্যবর্তী
        \ /
         a        ← a হলো minimal (নিচে কেউ নেই)
```

- যেসব node-এর উপরে কেউ নেই → Maximal element(s)
- যেসব node-এর নিচে কেউ নেই → Minimal element(s)
- যদি একজনই সবার উপরে থাকে → Greatest element
- যদি একজনই সবার নিচে থাকে → Least element

**Q35 এর Hasse Diagram বিশ্লেষণ:**
টেবিল থেকে বোঝা যায়:
- B1={a,b} → LUB={b}, GLB={a} ⇒ a নিচে, b উপরে
- B4={b,c} → LUB={c}, GLB={b} ⇒ b নিচে, c উপরে
- B6={c,d} → LUB={d}, GLB={c} ⇒ c নিচে, d উপরে

তাহলে Hasse Diagram:
```
        d           ← maximal (সর্বোচ্চ)
        |
        c
        |
        b
        |
        a           ← minimal (সর্বনিম্ন)
```
এটা একটা chain/linear order। a ≤ b ≤ c ≤ d

---

# 🔷 পার্ট ৩: Lattice (ল্যাটিস)

## Lattice কী?

> একটি Poset (Partial Order Set) কে **Lattice** বলা হয় যদি তার যেকোনো দুটি element-এর Least Upper Bound (LUB) এবং Greatest Lower Bound (GLB) থাকে।

```
Lattice = Poset যেখানে প্রতি pair (x,y) এর জন্য:
          - LUB (join, ∨) আছে
          - GLB (meet, ∧) আছে
```

## LUB (Least Upper Bound / Join / ∨)

দুটি element a, b এর **LUB বা join** হলো সবচেয়ে ছোট element যেটা a এবং b উভয়ের চেয়ে বড় (বা সমান)।

**Hasse Diagram এ বের করার নিয়ম:**
- a এবং b থেকে উপরে যাও, যেখানে first meet করবে সেটাই LUB

```
        d
       / \
      b   c
       \ /
        a

উদাহরণ: a ∨ b = b  (a থেকে উপরে b, b নিজেই → তাই b-ই LUB)
        b ∨ c = d   (b থেকে উপরে d, c থেকে উপরে d → d হলো LUB)
```

## GLB (Greatest Lower Bound / Meet / ∧)

দুটি element a, b এর **GLB বা meet** হলো সবচেয়ে বড় element যেটা a এবং b উভয়ের চেয়ে ছোট (বা সমান)।

**Hasse Diagram এ বের করার নিয়ম:**
- a এবং b থেকে নিচে যাও, যেখানে first meet করবে সেটাই GLB

```
উদাহরণ: b ∧ c = a  (b থেকে নিচে a, c থেকে নিচে a → a হলো GLB)
        b ∧ d = b   (b থেকে নিচে b, d থেকে নিচে b → b হলো GLB)
```

## Q35 এর টেবিল পূরণ:

Hasse Diagram: a → b → c → d (linear chain)

| Subset | LUB (∨) | GLB (∧) | ব্যাখ্যা |
|--------|---------|---------|----------|
| B1={a,b} | b | a | a ∨ b = b, a ∧ b = a |
| B2={a,c} | c | a | a ∨ c = c (c বড়), a ∧ c = a (a ছোট) |
| B3={a,d} | d | a | a ∨ d = d (d বড়), a ∧ d = a (a ছোট) |
| B4={b,c} | c | b | b ∨ c = c (c বড়), b ∧ c = b (b ছোট) |
| B5={b,d} | d | b | b ∨ d = d (d বড়), b ∧ d = b (b ছোট) |
| B6={c,d} | d | c | c ∨ d = d (d বড়), c ∧ d = c (c ছোট) |

---

# 🔷 পার্ট ৪: Digraph (ডাইগ্রাফ) এবং Adjacency Matrix

## Directed Graph (ডাইগ্রাফ) কী?

Digraph-এ edges-এর direction (দিক) থাকে। একটা edge <u,v> মানে u থেকে v-তে arrow যাচ্ছে।

## Adjacency Matrix (সংলগ্নতা ম্যাট্রিক্স)

Digraph-কে matrix আকারে প্রকাশ:

```
           TO →
           A  B  C  D
FROM ↓  A [0  1  0  1]
        B [0  0  1  0]
        C [1  0  0  1]
        D [0  1  1  0]
```

- M[i][j] = 1 মানে vertex i থেকে vertex j-তে edge আছে
- M[i][j] = 0 মানে vertex i থেকে vertex j-তে edge নেই

## In-degree (অন্তঃমাত্রা)

> কোনো vertex-এ **কয়টা arrow এসে পৌঁছায়** — সেটাই তার in-degree.

**ম্যাট্রিক্স থেকে বের করার নিয়ম:**
- ঐ vertex-এর **column** যোগ করো (উপর থেকে নিচে)

```
A-এর column: 0+0+1+0 = 1 → in-degree(A) = 1
B-এর column: 1+0+0+1 = 2 → in-degree(B) = 2
```

## Out-degree (বহির্মাত্রা)

> কোনো vertex থেকে **কয়টা arrow বের হয়ে যায়** — সেটাই তার out-degree.

**ম্যাট্রিক্স থেকে বের করার নিয়ম:**
- ঐ vertex-এর **row** যোগ করো (বাম থেকে ডানে)

```
A-এর row: 0+1+0+1 = 2 → out-degree(A) = 2
B-এর row: 0+0+1+0 = 1 → out-degree(B) = 1
```

## Q34 সমাধানের Strategy

Q34 তে Adjacency Matrix দেওয়া আছে (পরীক্ষার খাতায় ছবি থাকবে):

```
ধরো matrix টা এরকম:
     A  B  C  D
  A [a₁₁ a₁₂ a₁₃ a₁₄]
  B [a₂₁ a₂₂ a₂₃ a₂₄]
  C [a₃₁ a₃₂ a₃₃ a₃₄]
  D [a₄₁ a₄₂ a₄₃ a₄₄]
```

**পদ্ধতি:**

| Vertex | In-degree (কলাম যোগ) | Out-degree (রো যোগ) |
|--------|---------------------|---------------------|
| A | কলাম-১ এর যোগফল | রো-১ এর যোগফল |
| B | কলাম-২ এর যোগফল | রো-২ এর যোগফল |
| C | কলাম-৩ এর যোগফল | রো-৩ এর যোগফল |
| D | কলাম-৪ এর যোগফল | রো-৪ এর যোগফল |

**Check করার নিয়ম:** Total in-degree = Total out-degree = Total edges

**উদাহরণ matrix সহ:**

```
Matrix:
     A  B  C  D
  A [0  1  0  1]
  B [0  0  1  0]
  C [1  0  0  1]
  D [0  1  1  0]

উত্তর:
  Vertex A: in-degree = 1, out-degree = 2
  Vertex B: in-degree = 2, out-degree = 1
  Vertex C: in-degree = 2, out-degree = 2
  Vertex D: in-degree = 2, out-degree = 2

Verify: 1+2+2+2 = 7 = 2+1+2+2 ✓
```

---

# 🔷 পার্ট ৫: Q35 — Lattice ও Hasse Diagram (সম্পূর্ণ সমাধান)

## প্রদত্ত তথ্য বিশ্লেষণ:

টেবিল থেকে partial data:
- B1={a,b}: LUB={b}, GLB={a}  → a নিচে, b উপরে (a ≤ b)
- B4={b,c}: LUB={c}, GLB={b}  → b নিচে, c উপরে (b ≤ c)
- B6={c,d}: LUB={d}, GLB={c}  → c নিচে, d উপরে (c ≤ d)

## Hasse Diagram:

```
        d           ← Maximal element, Greatest element
        |
        c           ← Intermediate
        |
        b           ← Intermediate
        |
        a           ← Minimal element, Least element
```

এটা একটা **Total Order / Chain Lattice**!

## (1) Relation R কে Set আকারে প্রকাশ:

R-এ থাকবে সব pair (x,y) যেখানে x ≤ y (Hasse diagram অনুযায়ী)

```
R = {<a,a>, <b,b>, <c,c>, <d,d>,    ← reflexive pairs
     <a,b>, <a,c>, <a,d>,            ← a থেকে সবাই
     <b,c>, <b,d>,                    ← b থেকে c, d
     <c,d>}                           ← c থেকে d

মোট pair = 4 + 3 + 2 + 1 = 10
```

## (2) টেবিল পূরণ:

| Subset of A | LUB (∨) | GLB (∧) | কারণ |
|-------------|---------|---------|-------|
| B1={a, b} | {b} | {a} | b বড়, a ছোট |
| B2={a, c} | {c} | {a} | c বড়, a ছোট |
| B3={a, d} | {d} | {a} | d বড়, a ছোট |
| B4={b, c} | {c} | {b} | c বড়, b ছোট |
| B5={b, d} | {d} | {b} | d বড়, b ছোট |
| B6={c, d} | {d} | {c} | d বড়, c ছোট |

---

# 🔷 পার্ট ৬: Properties Check করার Shortcut Method (Matrix/Table থেকে)

## Relations-এর Properties Check (টেবিল/ম্যাট্রিক্স দিয়ে)

A = {a, b, c, d} এর উপর Relation R:

### ম্যাট্রিক্স তৈরি:

```
    a  b  c  d
a [ 1  1  0  0 ]   ← a-এর সম্পর্ক
b [ 0  1  1  0 ]   ← b-এর সম্পর্ক
c [ 0  0  1  1 ]   ← c-এর সম্পর্ক
d [ 0  0  0  1 ]   ← d-এর সম্পর্ক
```

### Properties চেক:

| Property | কী দেখতে হবে | Shortcut |
|----------|-------------|----------|
| **Reflexive** | Diagonal = সব 1? | Main diagonal check |
| **Irreflexive** | Diagonal = সব 0? | Main diagonal check |
| **Symmetric** | M[i][j] = M[j][i]? | Mirror image check |
| **Anti-symmetric** | M[i][j]=1 & M[j][i]=1 হলে i=j? | Mirror ≠ 1 |
| **Transitive** | M²-এর 1 গুলো M-এ আছে? | M² ⊆ M |

---

# 🔷 পার্ট ৭: গুরুত্বপূর্ণ সূত্র ও টিপস (Exam Quick Reference)

## ✅ Reflexive, Symmetric, Transitive মনে রাখার ছড়া:

> **R**eflexive → নিজের সাথে সম্পর্ক (**R** = নিজেকে দেখা)
> **S**ymmetric → দুই দিকে সমান (**S** = দুইপাশ সমান)
> **T**ransitive → চেইন কমপ্লিট (**T** = তিনটা connect)

## ✅ Equivalence = R + S + T

## ✅ Partial Order = R + A + T (A = Anti-symmetric)

## ✅ Lattice = Partial Order যেখানে প্রতি pair-এর LUB ও GLB আছে

## ✅ In-degree = Column sum, Out-degree = Row sum

## ✅ Hasse Diagram = Reflexive loops বাদ + Transitive edges বাদ + নিচ থেকে উপরে

## ✅ LUB = উপরে গিয়ে প্রথম মিলন = Join (∨)
## ✅ GLB = নিচে গিয়ে প্রথম মিলন = Meet (∧)

---

# 🔷 পার্ট ৮: Practice Problems (অনুশীলনী)

## Problem 1:
A = {1, 2, 3, 4}, R = {<1,2>, <2,3>, <1,3>, <4,4>}
Properties check করো।

**উত্তর:**
- Reflexive? → (1,1), (2,2), (3,3) নেই → ❌ NOT reflexive
- Irreflexive? → (4,4) আছে → ❌ NOT irreflexive
- Symmetric? → <1,2> আছে, <2,1> নেই → ❌ NOT symmetric
- Anti-symmetric? → কোনো opposite pair নেই → ✅ Anti-symmetric
- Transitive? → <1,2>+<2,3>→<1,3> আছে ✓, অন্য চেইন নেই → ✅ Transitive

## Problem 2:
Adjacency Matrix থেকে in/out-degree বের করো:
```
    A B C
A [ 0 1 1 ]
B [ 1 0 0 ]
C [ 0 1 0 ]
```

**উত্তর:**
- A: in = 1 (B→A), out = 2 (A→B, A→C)
- B: in = 2 (A→B, C→B), out = 1 (B→A)
- C: in = 1 (A→C), out = 1 (C→B)

## Problem 3:
Hasse Diagram: d ও e উপরে (কোনোটার উপর কেউ নেই), b ও c মাঝে, a নিচে।
```
      d     e
       \   /
        b c
         \|
          a
```
Subset {b,c} এর LUB ও GLB কত?

**উত্তর:** LUB নেই (b আর c-এর common upper bound কেউ নেই — d আর e কেউ সবার উপরে না)। GLB = a। তাই এটি Lattice নয়।

---

# 🔷 Quick Summary Table (দ্রুত রিভিশন)

| Concept | বাংলা | Check Method |
|---------|--------|-------------|
| Reflexive | প্রতিবর্তী | ∀a: (a,a) ∈ R |
| Irreflexive | অপ্রতিবর্তী | ∀a: (a,a) ∉ R |
| Symmetric | প্রতিসম | (a,b) ∈ R ⇒ (b,a) ∈ R |
| Anti-symmetric | প্রতি-প্রতিসম | (a,b)∈R ∧ (b,a)∈R ⇒ a=b |
| Transitive | সঙ্ক্রামক | (a,b)∈R ∧ (b,c)∈R ⇒ (a,c)∈R |
| Equivalence | সমতুল্যতা | Reflexive + Symmetric + Transitive |
| Partial Order | আংশিক ক্রম | Reflexive + Anti-symmetric + Transitive |
| In-degree | অন্তঃমাত্রা | Column যোগ |
| Out-degree | বহির্মাত্রা | Row যোগ |
| LUB / Join | সর্বনিম্ন ঊর্ধ্বসীমা | উপরে গিয়ে প্রথম meet |
| GLB / Meet | সর্বোচ্চ নিম্নসীমা | নিচে গিয়ে প্রথম meet |
| Maximal | আংশিক সর্বোচ্চ | যার উপরে কেউ নেই |
| Minimal | আংশিক সর্বনিম্ন | যার নিচে কেউ নেই |

---

> **পরীক্ষার জন্য শুভকামনা! 🍀 ইনশাআল্লাহ ভালো হবে।**
>
> **Remember:** প্রশ্ন ভালো করে পড়বে, matrix/table থেকে organize করে তথ্য বের করবে, step-by-step লিখবে, এবং শেষে verify করবে।


---

# 🔷 পার্ট ৯: সম্পূর্ণ পরীক্ষার উত্তরমালা (Answer Key)

## Section Ⅰ — Single Choice Questions (2×15 = 30)

### Q1. Compound Proposition চেনা
> **Ans: D** — "George Boole is not a boy" — এখানে "not" connective আছে তাই compound proposition।
> A, B, C — সব simple/atomic proposition (একটা মাত্র statement, কোনো connective নেই)।

### Q2. "if and only if" ↔ biconditional
> Statement: Two triangles are congruent **if and only if** three corresponding sides are equal.
> p ↔ q
> **Ans: p ↔ q** (biconditional)

### Q3. Predicate formula-এ variable y free নাকি bound?
> Predicate formula: A = ∀x P(x,y) — এখানে x quantified (bound), y quantified না → y **free**
> **Ans: A. free**

### Q4. Negation of "Not everyone likes flowers"
> Original: ¬(∀x: person(x) → likes_flowers(x))
> = "Not everyone likes flowers"
> Negation: ¬¬(∀x ...) = ∀x: person(x) → likes_flowers(x)
> = "Everyone likes flowers" = "All people like flowers"
> **Ans: A. All people like flowers**

### Q5. Sets A={1,2,3,4}, B={4,5,6}
> (i) Joint sets? → A∩B = {4} ≠ ∅ → joint/disjoint না (তারা intersect করে) 
>   
>   ⚠️ **সতর্কতা:** "joint sets" মানে disjoint (ছেদহীন) — A∩B = ∅ হলে disjoint। এখানে A∩B={4} আছে।
>   *(প্রসঙ্গ: কিছু textbook-এ "joint" মানে intersecting, আর "disjoint" মানে non-intersecting। প্রশ্নের ভাষায় "joint sets" বলতে intersecting বোঝাচ্ছে।)*
>
> যদি "joint" = intersecting (A∩B ≠ ∅): (i) True
> (ii) A∪B = {1,2,3,4,5,6} — singleton না → False
> (iii) Null set না → False
> (iv) |A∪B| = 6 → True
> ∴ (i) & (iv) True
> **Ans: B. (i) & (iv)**

### Q6. Equivalence Relation on A={a,b,c,d}
> Equivalence = Reflexive + Symmetric + Transitive
>
> A: {<a,b>,<a,a>,<b,a>,<b,b>,<c,c>,<d,d>}
> - Reflexive? (a,a),(b,b),(c,c),(d,d) → ✅
> - Symmetric? <a,b>→<b,a> আছে ✅
> - Transitive? চেইন চেক করো... <a,b>+<b,a>→<a,a> ✅, <b,a>+<a,b>→<b,b> ✅ → OK
> **Ans: A**

### Q7. A={1,2,3}, R={<1,2>,<2,3>,<1,3>}
> - Reflexive? (1,1),(2,2),(3,3) নেই → ✅ Irreflexive
> - Symmetric? <1,2> আছে <2,1> নেই → ❌
> - Anti-symmetric? কোনো (x,y)&(y,x) pair নেই → ✅
> - Transitive? <1,2>+<2,3>→<1,3> আছে ✅
> ∴ Irreflexive + Anti-symmetric + Transitive
> **Ans: C**

### Q8. Function চেনা (Arrow diagram)
> Function হতে গেলে: X-এর প্রতিটি element-এর কাছ থেকে **ঠিক একটি** arrow বের হবে Y-তে।
> (ছবি ছাড়া নির্দিষ্ট বলা যাচ্ছে না, কিন্তু condition: ∀x∈X, exactly one y∈Y)

### Q9. Strongly Connected Graph
> "path from a to b AND from b to a whenever a,b are vertices"
> এটাই strongly connected graph-এর definition।
> **Ans: C. strongly connected**

### Q10. Non-isomorphic graph (চিত্র ছাড়া)
> (চিত্র দেখে answer করতে হবে)

### Q11. Out-degree(v1) (চিত্র ছাড়া)
> **Ans: D. 3** (প্রশ্নপত্রে চিত্র অনুযায়ী)

### Q12. Euler + Hamilton Graph
> - Euler graph: সব vertex-এর degree even (undirected) / in=out (directed) + connected
> - Hamilton graph: সব vertex cover করে cycle আছে
> (চিত্র দেখে answer করতে হবে)

### Q13. Identity Element (অভেদ উপাদান)
> Table থেকে দেখো: e*e=e, e*a=a, e*b=b, e*c=c
> AND a*e=a, b*e=b, c*e=c
> e সবকিছুর সাথে operate করলে অপরটি unchanged → **e identity**
> **Ans: D. e**

### Q14. Associative Law (সহযোজন বিধি)
> Check: (a☉b)☉c = a☉(b☉c)
>
> A: a☉b = ab+a
>   LHS: (ab+a)☉c = (ab+a)c + (ab+a) = abc+ac+ab+a
>   RHS: a☉(bc+b) = a(bc+b)+a = abc+ab+a
>   LHS ≠ RHS → ❌
>
> B: a☉b = a+3b
>   LHS: (a+3b)☉c = (a+3b)+3c = a+3b+3c
>   RHS: a☉(b+3c) = a+3(b+3c) = a+3b+9c
>   LHS ≠ RHS → ❌
>
> D: a☉b = a
>   LHS: a☉c = a
>   RHS: a☉b = a
>   LHS = RHS = a → ✅ associative
> **Ans: D. a☉b = a**

### Q15. Binary Operation on N নয় কোনটি?
> N = Natural numbers = {0,1,2,3,...} বা {1,2,3,...}
> 
> A: a+b ∈ N → ✅
> B: a-b ∈ N?  2-5 = -3 ∉ N → ❌
> C: a ∈ N → ✅
> D: b ∈ N → ✅
> **Ans: B. a*b = a-b** (কারণ negative result হতে পারে)

---

## Section Ⅱ — True/False (1×10 = 10)

| Q | Answer | ব্যাখ্যা |
|---|--------|----------|
| 16 | **F** | Negation of "2+2=4" is "2+2≠4", not "2+2=5" |
| 17 | **T** | ¬(¬p∨q)∧q = (p∧¬q)∧q = p∧(¬q∧q) = p∧F = F — এটি contradiction! |
| | | অন্যদিকে: wff টা contradiction কিনা check করলে, ¬(¬p∨q)∧q = (p∧¬q)∧q = F |
| | | তাই "not a contradiction" = "এটা contradiction না" = False |
| | | **F** হবে! *(দেখে নিবে — প্রশ্ন বলছে "is not a contradiction" অর্থ contradiction না)* |
| 18 | **T** | ∀xP(x) → ∃xP(x): যদি সব x এর জন্য P(x) true, তাহলে কোনো x এর জন্য P(x) true |
| | | এটি logically valid (সত্য) |
| 19 | **T** | P(x) — এক variable (x) → one-place predicate |
| 20 | **F** | R-এ (a,b) আছে কিন্তু (b,a) নেই → symmetric না → equivalence না |
| 21 | **T** | f(x)=x²-4x+1 — quadratic, f(0)=1, f(4)=1 (অনেকে same output) → many-one ✓ |
| 22 | **T** | Tree definition: connected graph where m = n-1 |
| 23 | **T** | Handshaking Lemma: Σdeg(v) = 2|E| |
| 24 | **F** | Addition ও multiplication — দুটোই associative over ℝ! |
| 25 | **F** | X={0,1}: 1+1=2 ∉ X → closed না |

---

## Section Ⅲ — Fill in the Blanks (1×10 = 10)

### Q26. Proposition Logic Translation
> p: You have the flu, q: You miss the final exam, r: You pass the course
>
> **Statement 1:** q → ¬r (If you miss the exam, you will not pass)
> **Statement 2:** p ∨ q ∨ r (flu, or miss exam, or pass)

### Q27. Truth value
> P(x): x=5, Universe = {1,2,3,4}
> ∃x P(x) → "কোনো x এর জন্য x=5" → 5 সেটে নেই → **False / 0**

### Q28. Relations
> A={a,b,c}, R={<a,a>,<a,b>,<a,c>}, S={<a,a>,<b,a>}
>
> - Inverse of S = S⁻¹ = {<a,a>, <a,b>}
> - Power set of A = P(A) = {∅, {a}, {b}, {c}, {a,b}, {a,c}, {b,c}, {a,b,c}}
> - Function কোনটা? R — a-এর জন্য b ও c দুইটা image → function না। S — a→a, b→a, c-এর কোনো image নেই → function না (c থেকে arrow নেই)।
>   **S function না কারণ c-এর image নেই। R function না কারণ a-এর 2টা image।**
>   **দুটোর কোনোটাই function না।** কিন্তু যদি বলতে হয় কোনটা "closer to function" — S কারণ প্রতিটি element-এর সর্বোচ্চ একটা image (c বাদে, যার image নেই কিন্তু domain যদি A না হয়ে subset হতো...)।
>   প্রশ্ন: "Which is a function, R or S?" → **Neither** অথবা **None**

### Q29. Complement Graph & Planarity
> (চিত্র দেখে আঁকতে হবে)

### Q30. Binary Operation
> a*b = a (on ℤ)
> (-5)*(-5) = **-5**
> Commutative? a*b = a, b*a = b → a*b ≠ b*a যখন a≠b → **No**

---

## Section Ⅳ — Problem Solving (50 pts)

### Q31. Digital Logic Circuit (6 pts)
> (চিত্র ছাড়া — circuit diagram দেখে AND/OR/NOT gate চিহ্নিত করে expression লিখবে, তারপর truth table)

### Q32. Logical Proof (10 pts)
> Premises: ¬p∨q, r∨¬q, r→s
> Conclusion: p→s

**Proof:**
```
1. ¬p∨q        [Premise]
2. p→q         [Material Implication on 1]
3. r∨¬q        [Premise]
4. ¬q∨r        [Commutation on 3]
5. q→r         [Material Implication on 4]
6. r→s         [Premise]
7. q→s         [Hypothetical Syllogism on 5,6]
8. p→s         [Hypothetical Syllogism on 2,7]  ✓
```

### Q33. Sets & Relations (16 pts)
> U={a,b,c,d,e,f}, A={a,b,c,d}, B={c,d,e}
> R={<a,a>,<b,b>,<c,c>,<d,d>,<a,b>,<b,a>,<b,d>,<d,b>}

**(1) Bᶜ (complement of B wrt U):**
> Bᶜ = U \ B = {a, b, f}

**(2) A∩B:**
> A∩B = {c, d}

**(3) Bᶜ × (A∩B):**
> Bᶜ = {a, b, f}, A∩B = {c, d}
> Bᶜ × (A∩B) = {<a,c>, <a,d>, <b,c>, <b,d>, <f,c>, <f,d>}

**(4) Digraph of R:**
```
Nodes: a, b, c, d
Edges:
  a → a (loop), a → b, a ← b (b→a)
  b → b (loop), b → d, d → b (b←d)
  c → c (loop)
  d → d (loop)
```

**(5) Matrix MR:**
```
    a  b  c  d
a [ 1  1  0  0 ]
b [ 1  1  0  1 ]
c [ 0  0  1  0 ]
d [ 0  1  0  1 ]
```

**(6) Properties of R:**
- Reflexive? → (a,a),(b,b),(c,c),(d,d) সব আছে → ✅
- Symmetric? → <a,b>→<b,a> ✅, <b,d>→<d,b> ✅ → ✅
- Transitive? → <a,b>+<b,d>→<a,d> — কিন্তু <a,d> নেই! → ❌
- Anti-symmetric? → <a,b> & <b,a> আছে কিন্তু a≠b → ❌
- ∴ R is **Reflexive and Symmetric** but NOT Transitive, NOT Anti-symmetric

### Q34. In-degree & Out-degree (8 pts)
> Adjacency Matrix থেকে solve (পরীক্ষায় ছবি থাকবে)
> 
> **Strategy দেখো উপরে Part 4!**

### Q35. Lattice & Hasse Diagram (10 pts)
> **সম্পূর্ণ সমাধান উপরে Part 5 এ দেখো!**

---

# 🔷 পার্ট ১০: Last Minute Tips (শেষ মুহূর্তের পরামর্শ)

## পরীক্ষার হলে:

1. **Matrix দেওয়া থাকলে:** Row-wise out-degree, Column-wise in-degree — ৩০ সেকেন্ডের কাজ
2. **Relation properties:** Diagonal → reflexive/irreflexive, Mirror → symmetric, Chain → transitive
3. **Hasse Diagram থেকে LUB/GLB:** উপরে/নিচে গিয়ে first meet point — common sense!
4. **Truth Table:** 2ⁿ rows, systematic
5. **Proof:** প্রতিটি step-এ rule লিখবে (Premise, Modus Ponens, Hypothetical Syllogism ইত্যাদি)

## Common Mistakes:

| ভুল | সঠিক |
|-----|------|
| Reflexive-এ diagonal চেক না করা | Main diagonal always check |
| Anti-symmetric-এ (a,b)&(b,a) allow করে শুধু a=b হলে | a≠b হলে pair থাকবে না |
| LUB/GLB confuse | LUB = উপরে, GLB = নিচে |
| Adjacency matrix পড়তে ভুল | Row=FROM, Column=TO |
| Power set-এ ∅ ভুলে যাওয়া | P(A) তে ∅ always member |

---
