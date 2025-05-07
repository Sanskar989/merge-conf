

1. **Spun up a fresh repo**
   Opened GitHub, clicked that bright green “New Repository” button, and named it something quirky. Main branch was born.

2. **Dropped in a tiny webpage**
   Added a bare‑bones `index.html` and a splash of CSS—just enough to prove things work.

3. **Split the work into two ideas**

   * **Branch A – `feature/update-styling`**: “Let’s make this page look nicer.”
   * **Branch B – `feature/add-content`**: “Let’s write more words.”
     Both branched straight off `main`.

4. **Edited the same spot (uh‑oh!)**
   On each branch I changed the *exact* same `<div>`—one for color tweaks, the other for fresh text. I knew that would bite me later, and that was the point.

5. **Pushed and opened two PRs**
   Each branch got its own pull request. GitHub smiled politely and waited.

6. **Merged Branch A first**
   Styling PR went in clean. Main now had snazzy colors.

7. **Conflict time!**
   Tried merging the content PR… GitHub waved a big red ⚠️ “This branch has conflicts” banner. Yep—those overlapping lines collided.

8. **Pulled the branch locally and fixed it**

   ```bash
   git checkout feature/add-content
   git merge main          # brought in the conflicting changes
   # opened index.html, kept the best of both worlds,
   # deleted the >>>>>> / ======= / <<<<<< markers
   git add index.html
   git commit -m "Resolve merge conflict: combine new content with updated styling"
   git push
   ```

   In plain English: I kept the new text *and* the fresh colors, then tossed the conflict markers in the trash.

9. **GitHub turned green again**
   Refreshed the PR, saw “No conflicts with the base branch,” clicked **Merge**. Done!

10. **Happy ending**
    `main` now shows stylish colors *and* extra content. Two branches, one smooth webpage.
![Screenshot 2025-05-07 043656](https://github.com/user-attachments/assets/2a20cad0-180b-4ea5-a7a6-3a1bca365eca)
![Screenshot 2025-05-07 043556](https://github.com/user-attachments/assets/844de7e8-960a-4aaa-a548-beafcba2ceb9)
![Screenshot 2025-05-07 043508](https://github.com/user-attachments/assets/e34e1a28-59d8-4bb5-8dc8-6dfb656cf253)
![Screenshot 2025-05-07 043456](https://github.com/user-attachments/assets/1e53c16b-c6b3-4814-84a3-8b39ad30e4c4)
![Screenshot 2025-05-07 043426](https://github.com/user-attachments/assets/5fe7b457-623d-416d-b61b-3c4ec5631651)




