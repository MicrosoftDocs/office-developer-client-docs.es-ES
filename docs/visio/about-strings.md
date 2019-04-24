---
title: Cadenas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Las fórmulas pueden contener cadenas. Para dar formato a la presentación de una cadena, por ejemplo, en una celda que pide datos, el valor de un elemento de datos de formas o un campo de texto, se especifica una imagen de formato. El resultado puede tener formato de par número-unidad, cadena, fecha-hora, duración o moneda. Por ejemplo, el formato picture0 #/10 uuformats el par número-unidad 10.9 cm AS10 9/10 centímetros.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345069"
---
# <a name="about-strings"></a><span data-ttu-id="b3427-106">Cadenas</span><span class="sxs-lookup"><span data-stu-id="b3427-106">About Strings</span></span>

<span data-ttu-id="b3427-p102">Las fórmulas pueden contener cadenas. Para dar formato a la presentación de una cadena, por ejemplo, en una celda que pide datos, el valor de un elemento de datos de formas o un campo de texto, se especifica una imagen de formato. El resultado puede tener formato de par número-unidad, cadena, fecha-hora, duración o moneda. Por ejemplo, la imagen de formato "0 #/10 uu" muestra el par número-unidad 10,9 cm como "10 9/10 centímetros".</span><span class="sxs-lookup"><span data-stu-id="b3427-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="b3427-111">Puede usar imágenes de formato en la celda **Format** de la sección datos de formas y como argumento de la función **Format** o **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b3427-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="b3427-112">Al insertar un campo de texto, las imágenes de formato aparecen en la lista de formatos del cuadro de diálogo **Campo** (ficha **Insertar**).</span><span class="sxs-lookup"><span data-stu-id="b3427-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="b3427-113">Uso de funciones para dar formato a las cadenas</span><span class="sxs-lookup"><span data-stu-id="b3427-113">Using functions to format strings</span></span>

<span data-ttu-id="b3427-114">En cualquier fórmula que se resuelva en una cadena, incluidas las fórmulas de campo de texto personalizado, puede usar la función **Format** o **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b3427-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="b3427-115">La función FORMAT devuelve una cadena que contiene la salida con formato.</span><span class="sxs-lookup"><span data-stu-id="b3427-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="b3427-116">La función **FORMATEX** convierte la entrada sin escribir en las unidades que elija para el resultado con formato.</span><span class="sxs-lookup"><span data-stu-id="b3427-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="b3427-117">Presentación de datos de formas con formato</span><span class="sxs-lookup"><span data-stu-id="b3427-117">Displaying formatted shape data</span></span>

<span data-ttu-id="b3427-118">Para dar formato al valor mostrado de un elemento de datos de formas puede especificar una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="b3427-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="b3427-p105">Por ejemplo, una forma línea de tiempo de un proyecto puede tener una propiedad personalizada que mida el costo de un proceso. De forma predeterminada, el valor de un elemento de datos de formas es una cadena. Para dar formato a la cadena "1200", puede especificar "###.###,00 $" en la celda Format para que el usuario vea un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="b3427-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="b3427-122">Microsoft Visio usa las configuraciones de la ficha **Moneda** del cuadro de diálogo **Personalizar formato** del elemento de **configuración regional y de idioma** del Panel de control para determinar el símbolo de moneda y el separador de miles que debe mostrar.</span><span class="sxs-lookup"><span data-stu-id="b3427-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="b3427-123">(En el **Panel de control**, haga clic en **región e idioma**y, a continuación, haga clic en **configuración adicional**).</span><span class="sxs-lookup"><span data-stu-id="b3427-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="b3427-124">Para convertir una cadena en un valor de moneda que pueda utilizar posteriormente en cálculos, utilice la función CY.</span><span class="sxs-lookup"><span data-stu-id="b3427-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="b3427-125">Uso de funciones para manipular las cadenas de texto</span><span class="sxs-lookup"><span data-stu-id="b3427-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="b3427-p107">Puede utilizar funciones para manipular las cadenas de texto, por ejemplo, para localizar o sustituir determinados caracteres en una cadena. También puede obtener información acerca de la posición de un carácter en una cadena o identificar los caracteres iniciales y finales en una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="b3427-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

