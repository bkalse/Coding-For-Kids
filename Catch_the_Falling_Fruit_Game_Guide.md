
# 🎮 Game Project: Catch the Falling Fruit!

A fun and easy arcade-style game for 8-year-olds to learn coding and logic using **Scratch**.

---

## 🧰 Tools You’ll Need

- **Scratch Website:** [https://scratch.mit.edu](https://scratch.mit.edu)
- Works in browser, no install needed
- Drag-and-drop blocks – perfect for kids

---

## 🎯 Game Objective

Catch the falling fruits using a basket. You get a point for each fruit you catch. If you miss the fruit, you lose a life. The game ends when all lives are gone!

---

## 👣 Step-by-Step Instructions

### 1. Open Scratch

- Visit [https://scratch.mit.edu](https://scratch.mit.edu)
- Click **"Create"**

---

### 2. Add Sprites

- Delete the default **Cat** sprite
- Click **Choose a Sprite**
  - Select a **Basket** for the player
  - Choose a **Fruit** (like apple or banana)
- Resize the sprites if needed

---

### 3. Set the Background

- Click **Choose a Backdrop**
- Pick a colorful scene (like a garden or sky)

---

### 4. Code the Basket Movement

Click on the **Basket** sprite and add:

```scratch
when green flag clicked
go to x: 0 y: -130
forever
   if key (right arrow) pressed then
      change x by 10
   if key (left arrow) pressed then
      change x by -10
```

✅ This moves the basket left and right with the arrow keys.

---

### 5. Make the Fruit Fall

Click on the **Fruit** sprite and add:

```scratch
when green flag clicked
forever
   go to x: (pick random -200 to 200) y: 180
   repeat until <y position < -150>
      change y by -5
      wait 0.05 seconds
   end
```

✅ The fruit will drop from random positions at the top.

---

### 6. Detect Catching the Fruit

Still on the **Fruit** sprite:

```scratch
if <touching Basket> then
   play sound [pop v]
   change Score by 1
   go to x: (pick random -200 to 200) y: 180
```

- Create a new variable `Score`
- Add to the top:

```scratch
when green flag clicked
set Score to 0
```

---

### 7. Add Lives

- Create a new variable `Lives`
- Add:

```scratch
when green flag clicked
set Lives to 3
```

- Detect missed fruit:

```scratch
if <not touching Basket> and <y position < -150>> then
   change Lives by -1
```

- End the game when out of lives:

```scratch
if <Lives = 0> then
   stop all
```

---

### 8. Play and Improve

Let kids explore their creativity!

- Add more fruit types
- Make fruits fall faster over time
- Add sound effects and custom messages
- Draw their own basket and fruits

---

## 🧠 What You Learn

- **If, Repeat, Forever** logic
- **Coordinates and motion**
- **Scoring and lives with variables**
- **Game structure and interaction**
- **Creativity and problem solving**

---

## ✅ Challenge Ideas

- Add “bad” fruits (like bombs) that reduce score
- Add background music
- Make levels with faster speed

---

Happy coding! 🍎🧺🎉
