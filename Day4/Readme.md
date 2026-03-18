## Changes Implemented

This PR adds the complete practical implementation of Docker volumes and updates the README:

1. **Anonymous Volume**
   - Demonstrated creation and data persistence.
   - Data survives conta## Changes Implemented
 <img width="1907" height="802" alt="image" src="https://github.com/user-attachments/assets/0808474d-72ec-46d7-b997-5c6a1dd6b857" />
<img width="1107" height="580" alt="image" src="https://github.com/user-attachments/assets/48a7ed6b-2d4e-4017-9f50-4533333380db" />

2. **Named Volume**
   - Named volume (`mydata`) mapped to Nginx container.
   - Data persists even after container deletion and can be reused.
     <img width="1256" height="802" alt="image" src="https://github.com/user-attachments/assets/6f3026f4-c068-441b-a788-e2629b14b08e" />
      <img width="1907" height="802" alt="image" src="https://github.com/user-attachments/assets/1b97b5c7-371c-42e4-bdad-6023afb4f7a4" />
3. **Bind Mount**
   - Host folder (`~/myapp`) mapped to container path (`/usr/share/nginx/html`).
   - Live synchronization: changes on host reflect in container and vice versa.
