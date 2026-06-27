# 3D Container Planner PRO

An advanced web-based 3D visualization tool designed for logistics professionals, warehouse managers, and anyone involved in shipping and cargo planning. This application allows you to efficiently plan and optimize the loading of goods onto pallets and into standard shipping containers (20ft & 40ft), providing detailed cost and space analytics.

This tool is built with pure HTML, CSS (Tailwind), and JavaScript, utilizing the power of **Three.js** for interactive 3D rendering directly in your browser.

---

## ✨ Features

*   **Interactive 3D Scene**: A fully interactive 3D environment to visualize container loading.
    *   **Drag & Drop**: Easily position pallets inside the container.
    *   **Stacking**: Automatically stack pallets on top of each other.
    *   **Rotation**: Rotate pallets with a single keypress (`R`) to find the best fit.
    *   **Camera Controls**: Orbit (Right-click), Pan, and Zoom to inspect your cargo from any angle.
*   **Container & Pallet Selection**:
    *   Choose between standard **20ft** and **40ft** containers.
    *   Supports various pallet standards (EUR 1, EUR 2, etc.) and custom box sizes.
*   **Goods Catalog**:
    *   Define items with specific dimensions (L, W, H), weight, and individual packaging cost.
    *   Save defined goods to an in-memory catalog for quick reuse.
    *   **Import/Export**: Save your goods catalog to a JSON file and load it back in later sessions.
*   **Intelligent Optimization**:
    *   **Pallet Optimization**: Automatically calculates the optimal number of rows, columns, and layers for a given item on a selected pallet.
    *   **Custom Setup**: Specify a target quantity of parts, and the app will calculate and add the required number of fully-optimized pallets to meet your goal.
*   **Comprehensive Analytics Dashboard**:
    *   **Landed Cost Calculation**: Get an accurate "cost per piece" by factoring in packaging, pallet, wrapping, and freight costs.
    *   **SKU-level Costing**: See a detailed cost breakdown for each unique item (SKU) in the container.
    *   **Key Metrics**: Tracks total parts, total weight (tons), total volume (CBM), and container volume utilization percentage.
    *   **Cost Standards**: Switch between EU and CN cost profiles for packaging materials.
*   **Session Management**:
    *   **Save/Load Setup**: Export the entire container layout (pallet positions, contents, rotations) to a JSON file and import it to resume your work.
*   **Performance**:
    *   Uses `InstancedMesh` for efficient rendering of a large number of goods.
    *   A visual limit warning appears for pallets with more than 300 items to maintain smooth performance, while still including all items in the calculations.

---

## 🚀 How to Use

1.  **Select a Container**: Choose a 20ft or 40ft container. You can also input the estimated total freight cost for accurate landed cost calculation.
2.  **Define Your Goods**:
    *   In the "Goods Catalog" section, enter the dimensions (Length, Width, Height in cm), weight (kg), and packaging cost per piece for the item you want to load.
    *   Give it a name and click "Save" to add it to the dropdown catalog for the current session.
3.  **Configure a Pallet**:
    *   Select a pallet type from the "Pallet Loading" section.
    *   You can manually enter the rows, columns, and layers of goods.
4.  **Add Pallets to the Container**:
    *   **Optimize**: Click **Optimize** to let the app calculate the best packing configuration for the selected good on the pallet, then adds one pallet.
    *   **Build & Add**: Click **Build & Add** to create a pallet with the manual row/column/layer settings.
    *   **Custom Setup**: Enter a "Target Parts" number and click **Custom Setup**. The app will advise how many optimized pallets are needed and ask for confirmation before adding them.
5.  **Arrange the 3D Scene**:
    *   **Drag** pallets with the left mouse button to position them. They will snap to the grid and stack automatically.
    *   **Hover** over a pallet and press the **'R'** key to rotate it 90 degrees.
    *   **Double-click** a pallet to delete it.
6.  **Analyze the Results**:
    *   The "Cargo Status" panel updates in real-time.
    *   Review the total costs, weight, volume, and utilization to assess the efficiency of your plan.
    *   Use the "Save Setup" button to save your progress.

---

## 🛠️ Technical Stack

*   **3D Rendering**: Three.js (r128)
*   **UI/Styling**: Tailwind CSS
*   **Core Language**: JavaScript (ES6+)

The entire application is self-contained in a single `index.html` file, making it extremely portable and easy to run locally. Just open the file in any modern web browser.

---

## 📄 License

This project is open-source and available under the MIT License.

