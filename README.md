<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Simple Designed Page</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background: linear-gradient(to right, #74ebd5, #acb6e5);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .card {
      background-color: #fff;
      padding: 2rem;
      border-radius: 1rem;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      text-align: center;
      max-width: 400px;
      width: 100%;
    }

    .card h1 {
      color: #333;
      margin-bottom: 1rem;
    }

    .card p {
      color: #666;
      margin-bottom: 1.5rem;
    }

    .btn {
      padding: 0.75rem 1.5rem;
      background-color: #4e9af1;
      color: white;
      border: none;
      border-radius: 0.5rem;
      cursor: pointer;
      font-size: 1rem;
      transition: background-color 0.3s ease;
    }

    .btn:hover {
      background-color: #2e7bd8;
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Welcome!</h1>
    <p>This is a simple, stylish HTML page.</p>
    <button class="btn">Click Me</button>
  </div>
</body>
</html>
