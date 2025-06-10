<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quantum-Accelerated Imaging of N Stars</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #333;
            background-color: #f8f9fa;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            border-radius: 10px;
            margin-top: 20px;
            margin-bottom: 20px;
        }
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px 0;
            border-bottom: 2px solid #e9ecef;
        }
        .title {
            font-size: 2.5em;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 20px;
        }
        .authors {
            font-size: 1.2em;
            color: #555;
            margin-bottom: 10px;
        }
        .affiliation {
            font-size: 1em;
            color: #777;
            margin-bottom: 20px;
        }
        .links {
            margin-top: 20px;
        }
        .btn {
            display: inline-block;
            padding: 12px 24px;
            margin: 5px;
            background-color: #3498db;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #2980b9;
        }
        .btn.secondary {
            background-color: #95a5a6;
        }
        .btn.secondary:hover {
            background-color: #7f8c8d;
        }
        .section {
            margin: 40px 0;
        }
        .section h2 {
            font-size: 1.8em;
            color: #2c3e50;
            margin-bottom: 20px;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        .abstract {
            background-color: #f8f9fa;
            padding: 30px;
            border-radius: 8px;
            border-left: 4px solid #3498db;
            font-size: 1.1em;
            line-height: 1.7;
        }
        .key-results {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        .result-card {
            background-color: #fff;
            border: 1px solid #e9ecef;
            border-radius: 8px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .result-number {
            font-size: 2.5em;
            font-weight: 700;
            color: #e74c3c;
            margin-bottom: 10px;
        }
        .result-text {
            font-size: 1.1em;
            color: #555;
        }
        .method-overview {
            background-color: #ecf0f1;
            padding: 30px;
            border-radius: 8px;
            margin: 20px 0;
        }
        .code-block {
            background-color: #2c3e50;
            color: #ecf0f1;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            overflow-x: auto;
            margin: 20px 0;
        }
        .equation {
            text-align: center;
            margin: 20px 0;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 5px;
            font-family: 'Times New Roman', serif;
            font-size: 1.2em;
        }
        .figure-container {
            text-align: center;
            margin: 30px 0;
        }
        .figure-img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ddd;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            margin-bottom: 10px;
            background: white;
        }
        .figure-caption {
            color: #555;
            font-size: 1em;
            margin-top: 8px;
        }
        .citation-box {
            background-color: #f8f9fa;
            border: 1px solid #dee2e6;
            border-radius: 5px;
            padding: 20px;
            font-family: 'Courier New', monospace;
            font-size: 0.9em;
            margin: 20px 0;
        }
        .highlight {
            background-color: #fff3cd;
            padding: 2px 4px;
            border-radius: 3px;
        }
        @media (max-width: 768px) {
            .container {
                margin: 10px;
                padding: 15px;
            }
            .title {
                font-size: 2em;
            }
            .key-results {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 class="title">Quantum-Accelerated Imaging of N Stars</h1>
            <div class="authors">
                Fanglin Bao<sup>1,3</sup>, Hyunsoo Choi<sup>1</sup>, Vaneet Aggarwal<sup>2</sup>, and Zubin Jacob<sup>1,*</sup>
            </div>
            <div class="affiliation">
                <sup>1</sup>Birck Nanotechnology Center, School of Electrical and Computer Engineering, Purdue University<br>
                <sup>2</sup>School of Industrial Engineering, and School of Electrical and Computer Engineering, Purdue University<br>
                <sup>3</sup>baof@purdue.edu | <sup>*</sup>Corresponding author: zjacob@purdue.edu
            </div>
            <div class="links">
                <a href="#" class="btn">Paper (PDF)</a>
                <a href="#" class="btn secondary">Code</a>
                <a href="#" class="btn secondary">Supplementary</a>
            </div>
        </div>

        <div class="section">
            <h2>Abstract</h2>
            <div class="abstract">
                Imaging point sources with low angular separation near or below the Rayleigh criterion are important in astronomy, e.g., in the search for habitable exoplanets near stars. However, the measurement time required to resolve stars in the sub-Rayleigh region via traditional direct imaging is usually prohibitive. Here we propose <span class="highlight">quantum-accelerated imaging (QAI)</span> to significantly reduce the measurement time using an information-theoretic approach. QAI achieves quantum acceleration by adaptively learning optimal measurements from data to maximize Fisher information per detected photon. Our approach can be implemented experimentally by linear-projection instruments followed by single-photon detectors. We estimate the position, brightness, and the number of unknown stars <span class="highlight">10∼100 times faster</span> than direct imaging with the same aperture.
            </div>
        </div>

        <div class="section">
            <h2>Key Results</h2>
            <div class="key-results">
                <div class="result-card">
                    <div class="result-number">10-100×</div>
                    <div class="result-text">Faster than traditional direct imaging</div>
                </div>
                <div class="result-card">
                    <div class="result-number">Sub-Rayleigh</div>
                    <div class="result-text">Resolution below diffraction limit</div>
                </div>
                <div class="result-card">
                    <div class="result-number" style="color: #e74c3c; font-weight: bold;">Adaptive mode measurement</div>
                    <div class="result-text">to maximize quantum Fisher information per detected photon</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>Method Overview</h2>
            <div class="method-overview">
                <p><strong>Quantum-Accelerated Imaging (QAI)</strong> uses adaptive mode projection instead of direct pixel-based imaging. The key innovation is maximizing Fisher information per detected photon through optimal measurement strategies.</p>
                <div class="figure-container">
                    <img class="figure-img" src="Fig1.png" alt="Figure 1: QAI Schematic vs Direct Imaging">
                    <div class="figure-caption">Figure 1: QAI Schematic vs Direct Imaging (Adaptive Mode Projector → Single-photon Detectors).</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>Experimental Results</h2>
            <div class="figure-container">
                <img class="figure-img" src="Visualization1.gif" alt="Visualization of QAI's iterative scene estimation">
                <div class="figure-caption">Visualization of QAI's iterative scene estimation</div>
            </div>
            <div class="figure-container">
                <img class="figure-img" src="Fig3.png" alt="Figure 3: Acceleration Factors">
                <div class="figure-caption"> Acceleration of QAI — 10-100× speedup across different scenarios</div>
            </div>

        </div>

        <div class="section">
            <h2>Applications</h2>
            <ul style="font-size: 1.1em; line-height: 1.8;">
                <li><strong>Astronomy:</strong> Exoplanet detection, binary star systems</li>
                <li><strong>Microscopy:</strong> High-speed fluorescence imaging</li>
                <li><strong>Quantum Technology:</strong> Single-photon source characterization</li>
                <li><strong>Defense:</strong> Satellite tracking and identification</li>
            </ul>
        </div>

        <div class="section">
            <h2>Citation</h2>
            <div class="citation-box">
@article{bao2021quantum,
  title={Quantum-accelerated imaging of N stars},
  author={Bao, Fanglin and Choi, Hyunsoo and Aggarwal, Vaneet and Jacob, Zubin},
  journal={Optics Letters},
  volume={46},
  number={12},
  pages={2849--2852},
  year={2021},
  publisher={Optical Society of America},
  doi={10.1364/OL.430404}
}
            </div>
        </div>

        <div class="section">
            <h2>Acknowledgments</h2>
            <p>This work was supported by the Defense Advanced Research Projects Agency. The authors thank Bhargav Ganguly for discussions and S. Guha et al. from the University of Arizona for discussing their unpublished results on the N-star problem.</p>
        </div>
    </div>
</body>
</html>
