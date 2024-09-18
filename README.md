# Conway's Game of Life with CUDA and Tkinter in Jupyter Notebook

This project implements Conway's Game of Life with GPU acceleration using CUDA in a Jupyter Notebook environment, along with an interactive graphical interface created using `Tkinter`. The game logic is parallelized with `numba` and executed on a GPU, making it capable of efficiently handling larger grids. Users can manually select initial living cells via the graphical interface, after which the grid evolves according to Conway's rules.

## Features

- **GPU Acceleration**: Uses CUDA through the `numba` library to perform parallelized grid updates in Jupyter Notebooks.
- **Interactive GUI**: Built with `Tkinter`, the GUI allows users to drag and select living cells to set the initial state of the game.
- **Efficient Grid Processing**: Leverages GPU acceleration to run the Game of Life efficiently, even for large grid sizes.

## Requirements

To run this project, you need the following Python packages and dependencies:

- `Python 3.x`
- `Jupyter Notebook`: Install via `pip install notebook`
- `Numba`: For CUDA support, install via `pip install numba`
- `mpi4py`: For MPI parallel processing, install via `pip install mpi4py`
- `numpy`: For array manipulation, install via `pip install numpy`
- `Tkinter`: Usually included with most Python installations.

You will also need:

- **NVIDIA GPU**: with CUDA support (make sure to have CUDA-enabled drivers installed).
- **CUDA Toolkit**: Installed and configured to enable GPU acceleration.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/ShakyaDissanayake/Game-Of-Life-With-MPI4PY.git
    cd game-of-life-cuda-tkinter
    ```

2. **Create a virtual environment (optional but recommended)**:
    ```bash
    python -m venv gameoflifeenv
    source gameoflifeenv/bin/activate  # On Windows: gameoflifeenv\Scripts\activate
    ```

3. **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Install Jupyter Notebook**:
    ```bash
    pip install notebook
    ```

5. **Ensure CUDA is installed**:
    Verify that the CUDA toolkit is installed and properly configured on your system.

6. **Run the Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```

7. Open the notebook file (e.g., `game_of_life.ipynb`) and run the cells in order to interact with the program.

## How to Play

1. When the Jupyter notebook is launched, run the first few cells to initialize the game.
2. A Tkinter window will open, displaying an empty grid.
3. Click and drag on the grid to create initial living cells. Living cells will appear in bright green.
4. Press the "Start" button to begin the simulation.
5. The game will evolve according to Conway's rules, using GPU acceleration for grid processing.

## Customization

- **Grid Size**: You can customize the grid size and cell size in the `GameOfLifeGUI` class in the Jupyter Notebook code.
- **Color Customization**: The color of the living cells (currently bright green) can be changed by modifying the `draw_grid` method in `GameOfLifeGUI`.

## Conway's Game of Life Rules

1. Any live cell with fewer than two live neighbors dies, as if by underpopulation.
2. Any live cell with two or three live neighbors lives on to the next generation.
3. Any live cell with more than three live neighbors dies, as if by overpopulation.
4. Any dead cell with exactly three live neighbors becomes a live cell, as if by reproduction.

## Known Issues

- Ensure that you have a CUDA-enabled GPU and the appropriate drivers installed. Without CUDA support, the program will not function correctly.
- Tkinter GUI may not display properly within the Jupyter Notebook interface depending on the system setup. It’s recommended to run the GUI externally if any issues arise.

## Contributing

Feel free to submit pull requests or open issues if you find any bugs or have suggestions for improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

