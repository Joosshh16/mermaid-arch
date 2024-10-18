<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mermaid Diagram with Custom Icons</title>
    <script type="module">
      import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';

      mermaid.registerIconPacks([
        {
          name: 'logos',
          loader: () =>
            fetch('https://unpkg.com/@iconify-json/logos/icons.json').then((res) => res.json()),
        },
      ]);

      mermaid.initialize({ startOnLoad: true });
    </script>
</head>
<body>
    <div class="mermaid">
      graph TD
        A[API] -->|Call| B[Azure Function];
        B -->|Process| C[Azure Database];
        C -->|Store| D[Azure Storage];
        D -->|Return| A;
    </div>
</body>
</html>
