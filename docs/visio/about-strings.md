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
description: 'Las fórmulas pueden contener cadenas. Para aplicar el formato de salida de cadena, como en una celda prompt, un valor de elemento de datos de formas o un campo de texto, especifique un formato de imagen. Puede tener un formato de salida como un par de número de unidad, cadena, fecha y hora, duración o moneda. Por ejemplo, el uuformats de #/ 10 de formato picture0 la unidad de número par 10,9 cm as10 9/10 centímetros.'
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821489"
---
# <a name="about-strings"></a><span data-ttu-id="1b013-106">Cadenas</span><span class="sxs-lookup"><span data-stu-id="1b013-106">About Strings</span></span>

<span data-ttu-id="1b013-p102">Las fórmulas pueden contener cadenas. Para dar formato a la presentación de una cadena, por ejemplo, en una celda que pide datos, el valor de un elemento de datos de formas o un campo de texto, se especifica una imagen de formato. El resultado puede tener formato de par número-unidad, cadena, fecha-hora, duración o moneda. Por ejemplo, la imagen de formato "0 #/10 uu" muestra el par número-unidad 10,9 cm como "10 9/10 centímetros".</span><span class="sxs-lookup"><span data-stu-id="1b013-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="1b013-111">Puede utilizar imágenes de formato en la celda **Format** de la sección datos de formas y como un argumento a la función **FORMAT** o **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="1b013-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="1b013-112">Cuando se inserta un campo de texto, imágenes de formato aparecen en la lista de formatos en el cuadro de diálogo **campo** (ficha**Insertar** ).</span><span class="sxs-lookup"><span data-stu-id="1b013-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="1b013-113">Uso de funciones de cadenas de formato</span><span class="sxs-lookup"><span data-stu-id="1b013-113">Using functions to format strings</span></span>

<span data-ttu-id="1b013-114">Puede usar la función **FORMAT** o **FORMATEX** en cualquier fórmula que se resuelve en una cadena, incluidas las fórmulas de campo de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="1b013-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="1b013-115">La función FORMAT devuelve una cadena de la salida con formato.</span><span class="sxs-lookup"><span data-stu-id="1b013-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="1b013-116">La función **FORMATEX** convierte un argumento de entrada a las unidades que elija para el resultado con formato.</span><span class="sxs-lookup"><span data-stu-id="1b013-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="1b013-117">Mostrar datos de formas con formato</span><span class="sxs-lookup"><span data-stu-id="1b013-117">Displaying formatted shape data</span></span>

<span data-ttu-id="1b013-118">Para dar formato al valor mostrado de un elemento de datos de formas puede especificar una imagen de formato en la celda Format.</span><span class="sxs-lookup"><span data-stu-id="1b013-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="1b013-p105">Por ejemplo, una forma línea de tiempo de un proyecto puede tener una propiedad personalizada que mida el costo de un proceso. De forma predeterminada, el valor de un elemento de datos de formas es una cadena. Para dar formato a la cadena "1200", puede especificar "###.###,00 $" en la celda Format para que el usuario vea un valor de moneda.</span><span class="sxs-lookup"><span data-stu-id="1b013-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="1b013-122">Microsoft Visio usa la configuración en la ficha **moneda** en el cuadro de diálogo **Personalizar el formato** en el elemento **regional e idioma** en el Panel de Control para determinar el símbolo de moneda y miles separador que se debe mostrar.</span><span class="sxs-lookup"><span data-stu-id="1b013-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="1b013-123">(En el **Panel de Control**, haga clic en **idioma y región**y, a continuación, haga clic en **Configuración adicional**).</span><span class="sxs-lookup"><span data-stu-id="1b013-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="1b013-124">Para convertir una cadena en un valor de moneda que pueda utilizar posteriormente en cálculos, utilice la función CY.</span><span class="sxs-lookup"><span data-stu-id="1b013-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="1b013-125">Uso de funciones para manipular las cadenas de texto</span><span class="sxs-lookup"><span data-stu-id="1b013-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="1b013-p107">Puede utilizar funciones para manipular las cadenas de texto, por ejemplo, para localizar o sustituir determinados caracteres en una cadena. También puede obtener información acerca de la posición de un carácter en una cadena o identificar los caracteres iniciales y finales en una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="1b013-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

