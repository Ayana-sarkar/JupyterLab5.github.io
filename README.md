<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mastering JupyterLab</title>
    <style>
        /* Modern Reset & Variables */
        * {
            margin: 0;
            padding: 0;
            box-box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --accent-orange: #f97316;
            --accent-blue: #38bdf8;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
        }

        body {
            background-color:#052e16;
            color: #f0fdf4;
            line-height: 1.6;
        }

        /* Navbar */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 10%;
            background-color:#022c22;
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--text-main);
        }
        .logo span {
            color: var(--accent-orange);
        }
        .nav-links a {
            color: var(--text-muted);
            text-decoration: none;
            margin-left: 2rem;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: var(--accent-blue);
        }

        /* Hero Section */
        .hero {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 5rem 10%;
            min-height: 80vh;
        }
        .hero-content {
            max-width: 50%;
        }
        .hero-content h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 1.5rem;
        }
        .hero-content h1 span {
            color: var(--accent-orange);
        }
        .hero-content p {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 2rem;
        }
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, var(--accent-orange), #ea580c);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 20px rgba(249, 115, 22, 0.4);
        }

        /* Interactive Code Box Demo */
        .hero-visual {
            max-width: 45%;
            width: 100%;
        }
        .code-box {
            background-color: var(--card-bg);
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            border: 1px solid #334155;
        }
        .code-header {
            display: flex;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }
        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        .dot-red { background-color: #ef4444; }
        .dot-yellow { background-color: #eab308; }
        .dot-green { background-color: #22c55e; }
        
        .code-input {
            color: var(--accent-blue);
            font-family: 'Courier New', Courier, monospace;
            margin-bottom: 1rem;
        }
        .code-output {
            background-color: #0f172a;
            padding: 1rem;
            border-radius: 4px;
            border-left: 4px solid var(--accent-orange);
            font-family: monospace;
        }

        /* Curriculum Section */
        .curriculum {
            padding: 5rem 10%;
            background-color: #0b111e;
        }
        .curriculum h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
        }
       .grid,.row, [class*="card-container"], [class*="wrapper"]{
            display:flex !important;
            flex-direction: column !important;
            align-items: center !important;
            width: 100% !important; 
         }
       .card,[class*="box"], [class*="item"]{
            background-color: var(--card-bg);
            width: 100% !important;
            max-width: 800px !important;
            margin-bottom: 24px !important; 
            padding: 24px !important;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card h3 {
            color:#ffffff;
            margin-bottom: 1rem;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            color: var(--text-muted);
            border-top: 1px solid #1e293b;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column;
                text-align: center;
                padding-top: 2rem;
            }
            .hero-content {
                max-width: 100%;
                margin-bottom: 3rem;
            }
            .hero-visual {
                max-width: 100%;
            }
            .nav-links {
                display: none; /* Keep it simple for mobile */
            }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">🚀 Learn<span>Jupyter</span></div>
        <div class="nav-links">
            <a href=" https://ayana-sarkar.github.io/JupyterLab4.github.io/">JupyterLab4</a>
             <a href="https://ayana-sarkar.github.io/JupyterLab4.github.io/">JupyterLab4</a>
            <a href="https://ayana-sarkar.github.io/JupyterLab5.github.io/">JupiterLab5</a>
        </div>
    </nav>

    <section class="hero">
        <div class="hero-content">
            <h1>Master Data Science with <span>JupyterLab</span></h1>
            <p>Go from absolute beginner to writing interactive Python code, building data visualizations, and managing notebooks like a pro.</p>
            <a href="#curriculum" class="btn">Start Learning Free</a>
        </div>
        <div class="hero-visual">
            <div class="code-box">
                <div class="code-header">
                    <div class="dot dot-red"></div>
                    <div class="dot dot-yellow"></div>
                    <div class="dot dot-green"></div>
                </div>
                <div class="code-input">
                    <span style="color: #64748b;">[1]:</span> import pandas as pd<br>
                    <span style="color: #64748b;">[2]:</span> print("Welcome to JupyterLab!")
                </div>
                <div class="code-output">
                    Welcome to JupyterLab!
                </div>
            </div>
        </div>
    </section>

    <section id="curriculum" class="curriculum">
        <div class="grid">
            <div class="card">
                <h2>1.Least Squares</h2>
                <img src="Screenshot 2026-02-08 124349.png" alt="Data Visualization" class="box-image">
                <p>Line1: This imports everything (*) from pylab, a module that combines NumPy (for math/arrays) and Matplotlib (for plotting) into a single namespace.<br> 
                Line2-3: These lines create two Python lists containing your data points. $X$ holds the independent variables (inputs) and $Y$ holds the dependent variables (outputs). Each pair (e.g., $(0.0, 0.1)$, $(1.0, 0.9)$) represents a coordinate point on a graph.<br>
                Line4-5: Converts the standard lists into NumPy arrays (vectors). Standard Python lists can't do direct math (e.g., you can't multiply two lists together). Converting them to arrays unlocks "element-wise" math, allowing Python to multiply or add entire arrays at once.<br> 
                Line6-7: Computes the total sum of all elements in $X$ ($\sum X$) and all elements in $Y$ ($\sum Y$). These lines are much cleaner than using zip( ) . <br> 
                Line8: Computes the sum of squares ($\sum X^2$) . Xvec*Xvec multiplies each element by itself first, creating a new array [0.0, 1.0, 4.0, 9.0, 16.0, 25.0]. Then sum() adds them up to get 55.0.<br>
                Line 9: Squares the total sum of $X$ ($(\sum X)^2$).<br> 
                Example: Since sumX is $15.0$, this line calculates $15.0^2 = 225.0$.<br> 
                Line 10: Computes the sum of the products ($\sum XY$). Because they are vectors, Xvec*Yvec automatically multiplies corresponding elements together (e.g., $0.0 \times 0.1$, $1.0 \times 0.9$). Then sum() totals them up. <br> 
                 Line 11: n=len( Xvec )<br> 
                 Calculates the total number of data points by finding the length of the list $X$. Here, $n = 6$.<br> 
                 Line12-13 : Calculates the mathematical mean (average) of $X$ and $Y$ by dividing their sums by the total number of points ($n$). In statistics, these averages are denoted as $\bar{x}$ and $\bar{y}$.<br>
                 Line 14: Calculates the slope ($b$) of the best-fit line. This line uses an algebraic variation of the least-squares formula. It looks slightly different than your previous script, but mathematically simplifies to the exact same thing: <br> 
                 $$b = \frac{\sum XY - \frac{\sum X \sum Y}{n}}{\sum X^2 - \frac{(\sum X)^2}{n}}$$          <br> 
                 Line15: Calculates the y-intercept ($a$) using the calculated slope and means: $$a = \bar{y} - b\bar{x}$$<br>
                  <img src="Screenshot 2026-02-08 125457.png" alt="Data Visualization" class="box-image">
                 Line1: It takes the linear equation $y = a + bx$ and applies it to the entire Xvec array at once. For example, for $X=0$, it computes $0.029 + (0.989 \times 0)$. <br> 
                 around(..., 2) is a function from pylab/numpy that rounds the resulting numbers to 2 decimal places so they are clean and easy to read.<br>
                 Line2-3: The \t is a special character representing a tab space. It acts like hitting the Tab key on your keyboard, cleanly aligning the printed text output so the lists sit right next to each other.<br> 
                 Line4: Plots your original data points. 'ro' is shorthand for Red Circles (r = red, o = circle markers). This creates the red dots on the graph.<br>
                 Plots the calculated regression line. 'k-' is shorthand for a Black Solid Line (k stands for black in printing/plotting terms, - = solid line). Thus both curves are plotted on the same graph. <br></p>
            </div>
            <div class="card">
                <h2>2. Cells & Markdown</h2>
                <p>Learn the difference between Code and Markdown cells. Format notes with headers, lists, and math equations.</p>
            </div>
            <div class="card">
                <h2>3. Keyboard Shortcuts</h2>
                <p>Speed up your workflow drastically using Command and Edit modes, cell execution shortcuts, and deletions.</p>
            </div>
            <div class="card">
                <h2>4. Data & Visuals</h2>
                <p>Import CSVs, run Pandas operations, and render beautiful Matplotlib/Seaborn plots directly inside your notebook.</p>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 LearnJupyter Course. Built for future Data Scientists.</p>
    </footer>

</body>
</html>
