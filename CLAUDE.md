# Blog Matemático - Omar Alvarado Luna

## Información del Proyecto

- **Repositorio**: https://github.com/omaralvaradoluna/omaralvaradoluna.github.io
- **URL del sitio**: https://omaralvaradoluna.github.io
- **Dominio personalizado**: omaralvarado.mx (pendiente configuración DNS)
- **Directorio local**: /Users/omaralvarado/zen/math-blog

## Estructura del Proyecto

```
math-blog/
├── index.html              # Página principal del blog
├── cv.html                 # Curriculum Vitae
├── css/
│   └── theme.css           # Estilos centralizados del tema
├── images/                 # Imágenes de los artículos
├── articles/               # Artículos del blog
│   ├── homeostasis-rule110.html
│   └── collatz-turing-machine.html
└── CLAUDE.md               # Este archivo
```

## Tema y Estilo

### Paleta de Colores
- **Fondo oscuro**: #0a0a0f
- **Dorado principal**: #d4a853
- **Dorado sutil**: rgba(212, 168, 83, 0.3)
- **Acento púrpura**: #6366f1
- **Texto primario**: #ffffff
- **Texto secundario**: rgba(255,255,255,0.7)

### Tipografía
- **Títulos**: Playfair Display (serif elegante)
- **Cuerpo**: Inter (sans-serif legible)
- **Código/Mono**: JetBrains Mono

### Elementos de Diseño
- Efectos glassmorphism con blur
- Animaciones sutiles (float, fade-in, glow)
- Grid pattern de fondo con líneas doradas
- Cards con bordes dorados en hover
- Gradientes dorados en acentos

## Áreas de Investigación

1. **Complejidad Computacional** - Turing-completitud, indecidibilidad
2. **Autómatas Celulares** - Clasificación de Wolfram, Regla 110
3. **Cibernética** - Homeostasis, retroalimentación, Ley de Ashby
4. **Teoría de Números** - Conjetura de Collatz, primos
5. **Torah y Matemáticas** - Gematría, estructuras numéricas sagradas

---

## @publisher - Skill de Publicación

### Descripción
Skill para crear y publicar artículos en el blog matemático de Omar Alvarado.

### Tono y Estilo Narrativo

**OBLIGATORIO:** Todos los artículos deben seguir este tono:

> *"La arquitectura oculta de los sistemas que colapsan"*

**Estilo Isaac Asimov / Fundación:**
- **Determinismo estructural**: Los sistemas tienen destinos escritos en sus ecuaciones
- **Psicohistoria computacional**: Las matemáticas predicen el colapso inevitable
- **Frialdad analítica**: Sin sentimentalismos, solo estructuras y sus consecuencias
- **Inevitabilidad**: "No hay cuarta opción", "La única salida termodinámica"
- **Escala épica**: Hablar de civilizaciones, sistemas, colapsos globales

**Vocabulario preferido:**
- "Arquitectura oculta" en lugar de "estructura"
- "Colapso" en lugar de "falla"
- "Invariantes" en lugar de "propiedades"
- "Transición de fase" en lugar de "cambio"
- "Aniquilación de información" en lugar de "pérdida de datos"
- "Saturación computacional" en lugar de "sobrecarga"
- "Firma matemática irreducible" en lugar de "característica"

**Estructura narrativa:**
1. Plantear el sistema como un organismo con destino predeterminado
2. Revelar la estructura matemática subyacente (la "arquitectura oculta")
3. Demostrar por qué el colapso es inevitable (teoremas, ecuaciones)
4. Concluir con las únicas opciones disponibles (sin escapatoria romántica)

**Ejemplo de tono correcto:**
> "El nodo jerárquico no falla por incompetencia; colapsa porque su arquitectura computacional —un FSA de Nivel 3— carece del poder expresivo para contener la variedad de un sistema Turing-Completo. La ecuación de Ashby no perdona: H(R) < H(D). No hay voluntad que supere un teorema."

### Uso
```
@publisher publica en mi blog
@publisher haz un artículo con todo esto
@publisher crea un artículo sobre [tema]
```

### Comportamiento

Cuando el usuario invoque @publisher, el asistente debe:

1. **Recopilar el contenido** de la conversación actual relevante al artículo
2. **Estructurar el artículo** con:
   - Título principal
   - Subtítulo descriptivo
   - Introducción que enganche al lector
   - Secciones con H2 y H3
   - Ecuaciones matemáticas (usar KaTeX)
   - Código cuando sea relevante
   - Callouts para teoremas/conclusiones importantes
   - Referencias bibliográficas
3. **Generar visualizaciones** usando Wolfram cuando sea apropiado
4. **Crear el archivo HTML** en `/Users/omaralvarado/zen/math-blog/articles/`
5. **Actualizar index.html** para agregar el nuevo artículo a la lista
6. **Copiar imágenes** a `/Users/omaralvarado/zen/math-blog/images/`
7. **Commit y push** al repositorio

### Template de Artículo

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[TÍTULO] | Omar Alvarado</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
    <link rel="stylesheet" href="../css/theme.css">
    <style>
        .article-hero {
            padding: 160px 40px 80px;
            text-align: center;
            position: relative;
        }
        .article-hero::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 150px;
            height: 2px;
            background: var(--gradient-gold);
        }
        .back-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            font-size: 14px;
            color: var(--text-muted);
            margin-bottom: 40px;
            transition: color 0.3s ease;
        }
        .back-link:hover { color: var(--gold); }
        .article-tags {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 20px;
        }
        .article-hero h1 {
            max-width: 800px;
            margin: 0 auto 20px;
        }
        .article-subtitle {
            font-size: 1.3rem;
            color: var(--gold-dim);
            font-style: italic;
        }
        .article-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 30px;
            font-size: 14px;
            color: var(--text-muted);
        }
        .image-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: var(--spacing-lg) 0;
        }
        .image-grid figure { margin: 0; }
        .image-grid img { width: 100%; }
        @media (max-width: 700px) {
            .article-hero { padding: 120px 20px 60px; }
        }
    </style>
</head>
<body>

<div class="bg-animation"></div>
<div class="grid-overlay"></div>

<nav>
    <a href="../index.html" class="nav-logo"><span>א</span> OMAR ALVARADO</a>
    <ul class="nav-links">
        <li><a href="../index.html#articles">Artículos</a></li>
        <li><a href="../index.html#research">Investigación</a></li>
        <li><a href="../cv.html">CV</a></li>
        <li><a href="https://github.com/omaralvaradoluna" target="_blank">GitHub</a></li>
    </ul>
</nav>

<header class="article-hero">
    <a href="../index.html" class="back-link">← Volver al Inicio</a>
    <div class="article-tags">
        <span class="tag">[TAG1]</span>
        <span class="tag">[TAG2]</span>
        <span class="tag gold">Nuevo</span>
    </div>
    <h1>[TÍTULO DEL ARTÍCULO]</h1>
    <p class="article-subtitle">[SUBTÍTULO]</p>
    <div class="article-info">
        <span>[FECHA]</span>
        <span>•</span>
        <span>[X] min lectura</span>
    </div>
</header>

<article class="article-content">
    <!-- CONTENIDO DEL ARTÍCULO -->
</article>

<footer>
    <div class="footer-content">
        <div class="footer-brand"><span style="color: var(--gold);">א</span> Omar Alvarado Luna</div>
        <div class="footer-links">
            <a href="https://github.com/omaralvaradoluna" target="_blank">GitHub</a>
            <a href="https://medium.com/@alonsoluna" target="_blank">Medium</a>
            <a href="../cv.html">CV</a>
        </div>
        <div class="footer-copy">
            © 2026 Omar Alvarado Luna — Construido con matemáticas y curiosidad.
        </div>
    </div>
</footer>

<script src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script>
    // Renderizar ecuaciones con KaTeX
    // katex.render("ECUACIÓN", document.getElementById('eq1'), { displayMode: true });

    window.addEventListener('scroll', () => {
        document.querySelector('nav').classList.toggle('scrolled', window.scrollY > 50);
    });
</script>

</body>
</html>
```

### Template para Card en index.html

```html
<a href="articles/[SLUG].html" class="article-card">
    <div class="article-visual">
        <img src="images/[IMAGEN].png" alt="[ALT]">
    </div>
    <div class="article-content">
        <div class="article-tags">
            <span class="tag">[TAG1]</span>
            <span class="tag">[TAG2]</span>
            <span class="tag gold">Nuevo</span>
        </div>
        <h3>[TÍTULO]</h3>
        <p>[DESCRIPCIÓN BREVE]</p>
        <div class="article-equation">[ECUACIÓN PREVIEW]</div>
        <div class="article-meta">
            <span>[MES AÑO]</span>
            <span>•</span>
            <span>[X] min lectura</span>
            <span class="read-more">Leer artículo →</span>
        </div>
    </div>
</a>
```

### Comandos Git para Publicar

```bash
cd /Users/omaralvarado/zen/math-blog
git add .
git commit -m "Nuevo artículo: [TÍTULO]"
git push
```

### Checklist de Publicación

- [ ] Artículo HTML creado con todos los acentos correctos
- [ ] Imágenes generadas y copiadas a /images/
- [ ] Ecuaciones renderizadas con KaTeX
- [ ] Card agregada al index.html
- [ ] Quitar tag "Nuevo" de artículos anteriores si aplica
- [ ] Commit descriptivo creado
- [ ] Push al repositorio
- [ ] Verificar que el sitio se actualiza

---

## Notas Adicionales

- Usar siempre español con acentos correctos
- Mantener tono académico pero accesible
- Incluir referencias bibliográficas cuando sea apropiado
- Las imágenes de Wolfram Cloud expiran, descargarlas localmente
- El símbolo א (Aleph) es el logo del sitio
