---
title: Imágenes de formato
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251831
localization_priority: Normal
ms.assetid: df4c1c70-8b41-c046-7415-643188af0e06
description: Las imágenes de formato se utilizan para determinar cómo se muestra un valor. Por ejemplo, puede controlar el número de dígitos que aparecen a la derecha o a la izquierda del separador decimal o si una cadena de texto se muestra en mayúsculas o en minúsculas.
ms.openlocfilehash: 7043c9819f41ec2c08345c84010328be75677918
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436821"
---
# <a name="about-format-pictures"></a>Imágenes de formato

Las imágenes de formato se utilizan para determinar cómo se muestra un valor. Por ejemplo, puede controlar el número de dígitos que aparecen a la derecha o a la izquierda del separador decimal o si una cadena de texto se muestra en mayúsculas o en minúsculas.
  
> [!NOTE]
> Para definir una imagen de formato de fecha u hora usando el formato de Microsoft Office System, coloque la imagen entre llaves dobles, por ejemplo, "{{d/m/aa}}". Si usa un formato predefinido, por ejemplo, 201, escríbalo entre llaves y corchetes angulares, como este: "{ \< 201 \> }" 
  
En las secciones siguientes se muestran los símbolos que puede usar para dar formato a distintos tipos de valores para mostrar.
  
## <a name="string-and-numeric-values"></a>Cadenas y valores numéricos

|**Carácter**|**Descripción**|
|:-----|:-----|
|#  <br/> |Marcador de posición de dígito. Muestra un dígito o no muestra nada. Los ceros a la izquierda y a la derecha no se muestran. Si a la izquierda del decimal hay más dígitos que marcadores, se muestran todos los dígitos. Si a la derecha del decimal hay más dígitos que marcadores, la fracción se redondea al número total de marcadores. En el caso de una dimensión, si el marcador es el dígito situado más a la izquierda, no se muestran las subunidades distintas de cero.  <br/> Por ejemplo, FORMAT(0ft 11,25pda,"#,##u") muestra 11,25pda.  <br/> |
|0  <br/> |Marcador de posición de dígito (cero). Muestra un dígito o no muestra nada. Se muestran los ceros a la izquierda y a la derecha. Si a la izquierda del decimal hay más dígitos que marcadores, se muestran todos los dígitos. Si a la derecha del decimal hay más dígitos que marcadores, la fracción se redondea al número total de marcadores. En el caso de una dimensión, se muestran las subunidades que son cero.  <br/> Por ejemplo, FORMAT(2ft 11,33pda,"0,## u") muestra 2 ft 11,33 pda.  <br/> |
|.  <br/> |Marcador de posición decimal. Determina el número de dígitos que aparecen a la izquierda y a la derecha del separador decimal. En las unidades con varias partes, los decimales se aplican a la subunidad más pequeña (la situada más a la derecha). Muestra el carácter decimal definido en la **configuración regional y de idioma** del sistema (Panel de control).<br/> Por ejemplo, FORMAT(250 cm,"0,000 u") muestra 250,000 cm.  <br/> |
|,  <br/> |Separador de miles. Si está rodeado de marcadores de posición de dígitos (# ó 0), separa los miles de los cientos en los números que tengan cuatro o más dígitos a la izquierda del separador decimal. Muestra el separador de miles definido en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
|E- E+ e- e+  <br/> |Formato científico. Si el formato contiene al menos un marcador de posición de dígito a la derecha de estos símbolos, el número se muestra en formato científico. Inserta E o e entre el número y su exponente. En el caso de E+ o e+, se muestra el signo más (+) delante de los exponentes positivos y el signo menos (-) delante de los exponentes negativos. En el caso de E- o e-, sólo aparece el signo menos (-) cuando el exponente es negativo.  <br/> Por ejemplo, FORMAT(12345,67,"###,#e+#") muestra 123,5e+2.  <br/> |
|u o U  <br/> |Marcador de posición de etiqueta abreviada. Inserta indicadores de unidad abreviada después de cada subunidad. Por ejemplo: pda., pies, gra. El marcador de posición U inserta etiquetas de mayúsculas y minúsculas, mientras que el marcador de posición u inserta etiquetas en minúsculas. Inserta delante de la etiqueta el mismo número de espacios que hay delante del marcador de posición.  <br/> Por ejemplo, FORMAT(12 c 13 d,"#u") muestra 13c1.  <br/> |
|uu o UU  <br/> |Marcador de posición de etiqueta larga. Inserta etiquetas de unidad después de cada subunidad. Por ejemplo: pulgadas, pies, grados El marcador de posición U inserta etiquetas de mayúsculas y minúsculas, mientras que el marcador de posición u inserta etiquetas en minúsculas. Inserta delante de la etiqueta el mismo número de espacios que hay delante del marcador de posición.  <br/> Por ejemplo, FORMAT(12,43pda,"# #/4 UU") muestra 12 2/4 PULGADAS.  <br/> |
|uuu o UUU  <br/> |Marcador de posición de etiqueta universal. Inserta la forma universal (interna de Visio) de las etiquetas de unidad después de cada subunidad. El marcador de posición U inserta etiquetas de mayúsculas y minúsculas, mientras que el marcador de posición u inserta etiquetas en minúsculas. Inserta delante de la etiqueta el mismo número de espacios que hay delante del marcador de posición.  <br/> |
|/  <br/> |Marcador de posición de fracción. Muestra una expresión como un número entero con una fracción si hay un marcador de posición de dígito. En caso contrario, muestra sólo el número entero en el numerador. Si a continuación del marcador de posición de dígito del denominador hay un número, se redondea la fracción hasta la siguiente cuyo numerador sea 1 y se simplifica. Si en el denominador se especifica un número sin el marcador de posición de dígito, se redondea a la siguiente fracción, pero no se simplifica.  <br/> Por ejemplo, FORMAT(12,43,"# #/4") muestra 12 2/4.  <br/> |
|espacio  <br/> |Muestra un carácter de espacio en la salida con formato. Para mostrar otro carácter, use la barra diagonal inversa ( \) carácter.  <br/> |
   
## <a name="currency-values"></a>Valores de moneda

|**Carácter**|**Descripción**|
|:-----|:-----|
|$  <br/> |Símbolo de moneda. Muestra el símbolo de moneda definido en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
|u o U  <br/> |Marcador de posición de etiqueta abreviada. Inserta el símbolo estándar de la moneda local o la abreviatura de tres caracteres para las monedas no locales. Por ejemplo, $99,00, 42,70 FRF. El marcador de posición u inserta minúsculas y U inserta etiquetas de mayúsculas y minúsculas.  <br/> |
|uu o UU  <br/> |Marcador de posición de etiqueta larga. Inserta etiquetas de moneda largas detrás de cada subunidad. Por ejemplo: dólar USA, Franco francés. El marcador de posición u inserta minúsculas y U inserta etiquetas de mayúsculas y minúsculas.  <br/> |
|uuu o UUU  <br/> |Marcador de posición de etiqueta universal. Inserta las abreviaturas universales de tres caracteres para todas las monedas después de cada subunidad. Por ejemplo, 99,00 USD, 42,70 FRF. El marcador de posición u inserta minúsculas y U inserta etiquetas de mayúsculas y minúsculas. Inserta delante de la etiqueta el mismo número de espacios que hay delante del marcador de posición.  <br/> |
   
## <a name="text-values"></a>Valores de texto

|**Carácter**|**Descripción**|
|:-----|:-----|
|\  <br/> |Muestra el siguiente carácter tal y como es. Para mostrar el carácter de barra diagonal inversa, escriba \\ . Vea también "texto".  <br/> |
|"texto" o 'texto'  <br/> |Muestra el texto entre comillas tal y como es. Vea también \ (barra inversa).  <br/> |
|@  <br/> |Marcador de posición de texto. Reemplaza una cadena si el valor de una expresión es una cadena.  <br/> Por ejemplo, FORMAT("Hola", "'Ha escrito ('@')'") da como resultado "Ha escrito (Hola)".  <br/> |
|@+  <br/> |Marcador de posición de texto en mayúsculas. En el caso de valores de cadena, pasa el valor a mayúsculas.  <br/> Por ejemplo, FORMAT("Hola", "@ @+ @-") da como resultado "Hola HOLA hola".  <br/> |
|@-  <br/> |Marcador de posición de texto. En el caso de valores de cadena, pasa el valor a minúsculas.  <br/> Por ejemplo, FORMAT("Hola", "@ @+ @-") da como resultado "Hola HOLA hola".  <br/> |
   
## <a name="date-values"></a>Valores de fecha

|**Carácter**|**Descripción**|
|:-----|:-----|
|c o C  <br/> |Marcador de posición de fecha u hora. Muestra los valores de fecha y hora con formato corto (c) o largo (C), y el formato de hora genérico. Las versiones 4.0 y anteriores de Visio omiten este marcador de posición.  <br/> Por ejemplo: FORMAT(DATETIME("25/6/07 12:05"),"C") muestra lunes, 25 de junio de 2007 12:05:00 p.m. FORMAT(DATETIME("25 Jun 2007"),"c") muestra 25/6/07.  <br/> |
|/  <br/> |Separador de fecha. Si la expresión es una fecha, separa sus componentes. Muestra el separador de fecha definido en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
| [ ]  <br/> |Marcador de posición de fechas transcurridas. Se utiliza con los marcadores de posición d, dd y ww para mostrar las unidades de duración.  <br/> Por ejemplo, [d] o [dd] son los días transcurridos y [w] o [ww] son las semanas transcurridas.  <br/> |
|d  <br/> |Marcador de posición de día. Muestra el día como un número (de 1 a 31), sin cero a la izquierda.  <br/> |
|dd  <br/> | Marcador de posición de día. Muestra el día como un número (de 01 a 31), con cero a la izquierda.  <br/> |
|ddd o w  <br/> |Marcador de posición del día de la semana abreviado. Muestra el día abreviado (de Lun a Dom).  <br/> |
|dddd o w  <br/> |Marcador de posición del día de la semana sin abreviar. Muestra el día como un nombre completo (de lunes a domingo).  <br/> |
|ddddd  <br/> |Marcador de posición de fecha abreviada. Muestra una fecha con la forma corta definida en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
|dddd  <br/> |Marcador de posición de fecha sin abreviar. Muestra una fecha con la forma larga definida en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
|D  <br/> |Marcador de día para chino tradicional. Muestra el día del mes como una representación textual del número ordinal. Específico de la configuración regional.  <br/> |
|D_c  <br/> |Marcador de posición de día para chino tradicional. Muestra el día del mes como una representación textual del número ordinal. Independiente de la configuración regional del usuario.  <br/> |
|w_c o w_c  <br/> |Marcador de posición de día para chino tradicional. Independiente de la configuración regional del usuario.  <br/> |
|w_e  <br/> |Marcador de posición del día de la semana abreviado en inglés. Muestra el día abreviado (de Sun a Sat). Independiente de la configuración regional del usuario.  <br/> |
|w_j  <br/> |Marcador de posición del día de la semana abreviado en japonés. Muestra el día abreviado. Independiente de la configuración regional del usuario.  <br/> |
|w_k  <br/> |Marcador de posición del día de la semana abreviado en coreano. Muestra el día abreviado. Independiente de la configuración regional del usuario.  <br/> |
|w_s o w_s  <br/> |Marcador de posición de día para chino simplificado. Independiente de la configuración regional del usuario.  <br/> |
|ww_e  <br/> |Marcador de posición del día de la semana sin abreviar en inglés. Muestra el día como un nombre completo (de Sunday a Saturday). Independiente de la configuración regional del usuario.  <br/> |
|ww_j  <br/> |Marcador de posición del día de la semana sin abreviar en japonés. Muestra el día como un nombre completo. Independiente de la configuración regional del usuario.  <br/> |
|w_k  <br/> |Marcador de posición del día de la semana sin abreviar en coreano. Muestra el día como un nombre completo. Independiente de la configuración regional del usuario.  <br/> |
|M  <br/> |Marcador de posición de mes. Muestra el mes como un número (de 1 a 12), sin cero a la izquierda. Vea también m (marcador de posición de minutos).  <br/> |
|MM  <br/> |Marcador de posición de mes. Muestra el mes como un número (de 01 a 12), con cero a la izquierda. Vea también mm (marcador de posición de minutos).  <br/> |
|MMM  <br/> |Marcador de posición de mes. Muestra el mes en forma abreviada (de Ene a Dic).  <br/> |
|MMMM  <br/> |Marcador de posición de mes. Muestra el nombre completo del mes (de enero a diciembre).  <br/> |
|MMMM_c  <br/> |Marcador de posición del mes en chino tradicional. Muestra el nombre completo del mes. Independiente de la configuración regional del usuario.  <br/> |
|MMMM_e  <br/> |Marcador de posición del mes en inglés. Muestra el nombre completo del mes. Independiente de la configuración regional del usuario.  <br/> |
|yy  <br/> |Marcador de posición de año. Muestra el año como un número de dos dígitos (de 00 a 99).  <br/> |
|yyyy  <br/> |Marcador de posición de año. Muestra el año como un número de cuatro dígitos (de 1900 a 2078).  <br/> |
|g  <br/> |Marcador de posición de año. Específico de la configuración regional. En japonés, muestra la versión abreviada para la era Gengo. En coreano, muestra la etiqueta del año coreano, seguida de un espacio.  <br/> |
|g_j  <br/> |Marcador de posición de año. En japonés, muestra la versión abreviada para la era Gengo. Independiente de la configuración regional del usuario.  <br/> |
|gg o G  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra la versión abreviada de la etiqueta del año. En japonés, muestra la versión abreviada para la era Gengo en Kanji. En coreano, muestra la etiqueta del año coreano, seguida de un espacio.  <br/> |
|gg_c  <br/> |Marcador de posición de año. En chino tradicional, muestra la versión abreviada de la etiqueta del año. Independiente de la configuración regional del usuario.  <br/> |
|gg_j  <br/> |Marcador de posición de año. En japonés, muestra la versión abreviada para la era Gengo en Kanji. Independiente de la configuración regional del usuario.  <br/> |
|gg_k  <br/> |Marcador de posición de año. En coreano, muestra la etiqueta del año coreano, seguida de un espacio. Independiente de la configuración regional del usuario.  <br/> |
|ggg o GG  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra la versión completa de la etiqueta del año. En japonés, muestra la versión completa para la era Gengo en Kanji. En coreano, muestra la etiqueta del año coreano, seguida de un espacio.  <br/> |
|ggg_c  <br/> |Marcador de posición de año. En chino tradicional, muestra la versión completa de la etiqueta del año. Independiente de la configuración regional del usuario.  <br/> |
|ggg_j  <br/> |Marcador de posición de año. En japonés, muestra la versión completa para la era Gengo en Kanji. Independiente de la configuración regional del usuario.  <br/> |
|e  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra la cadena que representa el año Juliano. En japonés, muestra el año Gengo como uno o dos dígitos, sin cero a la izquierda. En coreano, muestra el año coreano como un número arábigo de cuatro dígitos.  <br/> |
|e_c  <br/> |Marcador de posición de año. En chino tradicional, muestra la cadena que representa el año juliano. Independiente de la configuración regional del usuario.  <br/> |
|e_j  <br/> |Marcador de posición de año. En japonés, muestra el año Gengo como uno o dos dígitos arábigos. Independiente de la configuración regional del usuario.  <br/> |
|e_k  <br/> |Marcador de posición de año. En coreano, muestra el año coreano como un número arábigo de cuatro dígitos. Independiente de la configuración regional del usuario.  <br/> |
|E  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra la cadena que representa el año de la república. En japonés, muestra el año Gengo como uno o dos dígitos, sin cero a la izquierda. En coreano, muestra el año coreano como un número arábigo de cuatro dígitos.  <br/> |
|E_c  <br/> |Marcador de posición de año. En chino tradicional, muestra la cadena que representa el año de la república. Independiente de la configuración regional del usuario.  <br/> |
|ee  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra la cadena que representa el año Juliano. En japonés, muestra el año Gengo como uno o dos dígitos arábigos, con un cero a la izquierda si es necesario. En coreano, muestra el año coreano como un número arábigo de cuatro dígitos.  <br/> |
|ee_j  <br/> |Marcador de posición de año. En japonés, muestra el año Gengo con dos dígitos arábigos. Independiente de la configuración regional del usuario.  <br/> |
|EE  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra la cadena que representa el año de la república. En japonés, muestra el año Gengo como uno o dos dígitos arábigos, con un cero a la izquierda si es necesario. En coreano, muestra el año coreano como un número arábigo de cuatro dígitos.  <br/> |
|n o N  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra el año de la república como un número arábigo. En japonés, muestra el año Gengo como uno o dos dígitos, sin cero a la izquierda. En coreano, muestra el año coreano como un número arábigo de cuatro dígitos.  <br/> |
|n_c  <br/> |Marcador de posición de año. En chino tradicional, muestra el año de la república como un número arábigo. Independiente de la configuración regional del usuario.  <br/> |
|nn o NN  <br/> |Marcador de posición de año. Específico de la configuración regional. En chino tradicional, muestra el año de la república como un número arábigo. En japonés, muestra el año Gengo como uno o dos dígitos arábigos, con un cero a la izquierda si es necesario. En coreano, muestra el año coreano como un número arábigo de cuatro dígitos.  <br/> |
   
## <a name="time-values"></a>Valores de hora

|**Carácter**|**Descripción**|
|:-----|:-----|
|:  <br/> |Separador de hora. Muestra la hora definida en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
|[ ]  <br/> |Marcador de posición de tiempo transcurrido. Se utiliza con los marcadores de posición h, hh, m, mm, s y ss para mostrar las unidades de duración. Por ejemplo, [h] o [hh] son las horas, [m] o [mm] los minutos y [s] o [ss] los segundos transcurridos.  <br/> |
|h  <br/> |Marcador de posición de hora. Muestra la hora sin cero a la izquierda, en formato de 12 horas (de 0 a 12).  <br/> |
|hh  <br/> |Marcador de posición de hora. Muestra la hora con cero a la izquierda, en formato de 12 horas (de 00 a 12).  <br/> |
|H  <br/> |Marcador de posición de hora. Muestra la hora sin cero a la izquierda, en formato de 24 horas (de 0 a 24).  <br/> |
|HH  <br/> |Marcador de posición de hora. Muestra la hora con cero a la izquierda, en formato de 24 horas (de 00 a 24).  <br/> |
|m  <br/> |Marcador de posición de minuto. Muestra los minutos sin cero a la izquierda (de 0 a 59).  <br/> |
|mm  <br/> |Marcador de posición de minuto. Muestra los minutos con cero a la izquierda (de 00 a 59).  <br/> |
|s  <br/> |Marcador de posición de segundo. Muestra los segundos sin cero a la izquierda (de 0 a 59).  <br/> |
|ss  <br/> |Marcador de posición de segundo. Muestra los segundos con cero a la izquierda (de 00 a 59).  <br/> |
|t  <br/> |Abreviatura a.m. o p.m. Muestra la abreviatura definida en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
|tt  <br/> |Indicador de a.m. o p.m. Muestra el indicador completo definido en la **configuración regional y de idioma** del sistema (Panel de control).<br/> |
|t_c o tt_c  <br/> |Indicador a.m. o p.m. en chino tradicional. Muestra el indicador. Independiente de la configuración regional del usuario.  <br/> |
|t_k o tt_k  <br/> |Indicador a.m. o p.m. en coreano. Muestra el indicador. Independiente de la configuración regional del usuario.  <br/> |
|t_j o tt_j  <br/> |Indicador a.m. o p.m. en japonés. Muestra el indicador. Independiente de la configuración regional del usuario.  <br/> |
|t_e  <br/> |Indicador a.m. o p.m. en inglés. Muestra el indicador abreviado. Independiente de la configuración regional del usuario.  <br/> |
|tt_e  <br/> |Indicador a.m. o p.m. en inglés. Muestra el indicador completo. Independiente de la configuración regional del usuario.  <br/> |
|t_s o tt_s  <br/> |Indicador a.m. o p.m. en chino simplificado. Muestra el indicador. Independiente de la configuración regional del usuario.  <br/> |
|T  <br/> |Formato de hora general.  <br/> |
   

