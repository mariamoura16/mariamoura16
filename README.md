from pptx import Presentation

# Cria uma apresentação
prs = Presentation()

# Adiciona um slide com o layout de título e subtítulo
slide_layout = prs.slide_layouts[0]
slide = prs.slides.add_slide(slide_layout)

# Adiciona um título e subtítulo
title = slide.shapes.title
subtitle = slide.placeholders[1]

title.text = "Título da Apresentação"
subtitle.text = "Subtítulo da Apresentação"

# Adiciona outro slide com layout de título e conteúdo
slide_layout = prs.slide_layouts[1]
slide = prs.slides.add_slide(slide_layout)

title = slide.shapes.title
content = slide.placeholders[1]

title.text = "Título do Slide"
content.text = "Conteúdo do Slide"

# Salva a apresentação
prs.save('minha_apresentacao.pptx')
