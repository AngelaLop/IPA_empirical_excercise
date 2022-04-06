Este repositorio contiene los datos para el ejercicio empírico de la posición de Student volunteer - Codewords Guatemala. Los candidatos pueden clonar este repositorio para acceder a los datos y recursos necesarios para su desarrollo. 
La data comprende información estructurada y no estructurada de una pequeña encuesta telefónica realizada como parte de un experimento para medir el impacto que diferentes metodologías de recolección de información tienen sobre el reporte de marcadores de empoderamiento. El repositorio contiene una base de datos .dta donde además de la identificación de las encuestadas y algunas características sociodemográficas, cuenta con tres brazos de tratamiento: el primero, identifica las encuestas donde las preguntas de empoderamiento fueron recolectadas de forma tradicional (“directo”), el segundo identifica las encuestas que fueron hechas aumentando el nivel de privacidad para encuestadas marcando la opción elegida directamente en el teclado del teléfono de la encuestada (“marcación”) y el tercero que identifica aquellas encuestas que se contestaron mediante el uso de una palabra código (“palabra codigo”). Para el segundo brazo, las respuestas se encuentran grabadas en tres archivos de audio .mp3, nombrados con el correspondiente ID de las encuestadas.  
# Como usar este repositorio
La base de datos de la encuesta se encuentra en la carpeta Data/empowerment_experiment_demo.dta. Los audios del segundo brazo de la encuesta se encuentran en la carpeta Audios 
Por favor no envíe ninguna respuesta haciendo push ni commits a este repositorio pues otros candidatos podrían ver su trabajo. 
# Codebook
``` caseid “numero de identificación de la encuestada"
    treatment "brazo de tratamiento asignado" "1=directo/2=marcación/3=palabra codigo"
    home_11 " ¿Quién es el jefe de hogar en su hogar?"
    home_12 " ¿Cuál es el nivel de educación más alto que Ud. aprobó?" 
    home_17 " ¿Cuál es su estado civil actual?" 
    empowerment_1c "¿Se le permite ir sola para reunirse con sus amiga y amigos por cualquier razón, para conversar o almorzar? Brazo3" "Yes=1/No=2"
    empowerment_1t  "¿Tiene que pedir permiso para comprar frutas o verduras, medicamentos o suministros personales?" "Yes=1/No=2 Brazo1"
    empowerment_2c “¿Se le permite ir sola para reunirse con sus amiga y amigos por cualquier razón, para conversar o almorzar? Brazo3" "Yes=1/No=2"
    empowerment_2t  "¿Tiene que pedir permiso para comprar frutas o verduras, medicamentos o suministros personales?"  "Yes=1/No=2 Brazo1"
    file_audio_empowerment "nombre del audio al que corresponde la encuesta" 

# ¿En qué consiste el ejercicio?
1.	Por favor clone el repositorio.
2.	Cree un código (R, Stata, Python, su preferencia) que haga:
a. Lea la base empowerment_experiment_demo.dta.
d. Identifique los tres brazos de tratamiento y las preguntas de empoderamiento empowerment_t y empowerment_c para el brazo 1 y 3, respectivamente.
e. Cree los marcadores de empoderamiento empowerment_a (1 y 2) para el segundo brazo, procesando la información contenida en los audios. Para esto, puede hacer uso del repositorio https://github.com/ribt/dtmf-decoder.git o cualquier decodificador de audio de su preferencia. 
f.Cree un codigo (Phyton, R, Stata o el lenguaje de su preferencia) que muestre los pasos utilizandos para la decodificación del audio, la creación de la base de datos estructurada con las respectivas respuestas y el pegue de las mismas con la base de datos empowerment_experiment_demo.dta.
