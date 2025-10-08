# Part 3 — Robot Manager (Make it Interactive)

- **Timebox:** ~45 minutes

## 📝 Brief

You’re seeing a basic **“robot manager”** UI. It’s a **draft from an external UX designer**.  
Your task is to **make it interactive** so we can test basic functionality.

## ✅ Todos (Suggested Order)

1. Replace the **hard-coded cards** with a loop that renders from the existing `products` data
2. Add **state to control the modal** and wire up the “Add Product” button to open it
3. Make the modal **closable** (close button and after submission)
4. Add **form bindings** so the input fields store their values
5. On form submission, **create a new robot** and **add it to the list**
6. Handle **tags** by splitting a comma-separated list
7. Ensure images work by simply using the entered **URL**

## 🧩 Notes & Gaps to Address

- You’ll need some reactive state to control the modal and the form
- The form should not reload the page on submit
- New robots should have a unique identifier
- For tags, trimming and splitting is enough — no advanced parsing needed
- The data doesn’t need to persist after reload
- The layout and styling are already mostly set up — focus on interaction, not design