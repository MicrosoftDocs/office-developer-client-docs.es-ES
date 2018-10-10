---
title: Usar caracteres comodín en comparaciones de cadenas
TOCTitle: Using Wildcard Characters in String Comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73946560d06d12c9bdb72b41ce0f560ad9df3e65
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484322"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="03f23-102">Usar caracteres comodín en comparaciones de cadenas</span><span class="sxs-lookup"><span data-stu-id="03f23-102">Using Wildcard Characters in String Comparisons</span></span>


<span data-ttu-id="03f23-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="03f23-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="03f23-p101">La coincidencia de patrones integrada proporciona una herramienta versátil para realizar comparaciones de cadenas. En la siguiente tabla, se muestran los caracteres comodín que puede usar con el operador **Like** y el número de dígitos o cadenas con los que se corresponden.</span><span class="sxs-lookup"><span data-stu-id="03f23-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03f23-106">Caracteres en <em>patrón</em></span><span class="sxs-lookup"><span data-stu-id="03f23-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="03f23-107">Correspondencia en <em>expresión</em></span><span class="sxs-lookup"><span data-stu-id="03f23-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03f23-p102">? o _ (subrayado)</span><span class="sxs-lookup"><span data-stu-id="03f23-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="03f23-110">Cualquier carácter</span><span class="sxs-lookup"><span data-stu-id="03f23-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03f23-111">\*o %</span><span class="sxs-lookup"><span data-stu-id="03f23-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="03f23-112">Cero o más caracteres</span><span class="sxs-lookup"><span data-stu-id="03f23-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="03f23-113">Un único dígito (0 – 9)</span><span class="sxs-lookup"><span data-stu-id="03f23-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03f23-114">[<em>listaDeCaracteres</em>]</span><span class="sxs-lookup"><span data-stu-id="03f23-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="03f23-115">Cualquier carácter de <em>listaDeCaracteres</em></span><span class="sxs-lookup"><span data-stu-id="03f23-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>listaDeCaracteres</em>]</p></td>
<td><p><span data-ttu-id="03f23-117">Cualquier carácter no incluido en <em>listaDeCaracteres</em></span><span class="sxs-lookup"><span data-stu-id="03f23-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03f23-118">Puede utilizar un grupo de uno o varios caracteres (*listacaracteres*) entre corchetes (\[ \]) para que coincida con cualquier carácter único en *expresión* y *listacaracteres* puede incluir casi cualquier carácter en el carácter ANSI establecidas, incluyendo dígitos.</span><span class="sxs-lookup"><span data-stu-id="03f23-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="03f23-119">Puede usar los caracteres especiales corchete de apertura (\[ ), el signo de interrogación (?), signo de número (\#) y el asterisco (\*) para que coincida con ellos mismos directamente sólo si están entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="03f23-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="03f23-120">No se puede usar el corchete de cierre ( \]) dentro de un grupo para que coincida con sí mismo, pero se puede usar fuera de un grupo como un carácter individual.</span><span class="sxs-lookup"><span data-stu-id="03f23-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="03f23-121">Además de una lista simple de caracteres incluidos entre corchetes, *listacaracteres* puede especificar un intervalo de caracteres mediante un guión (-) para separar la parte superior y los límites inferiores del rango.</span><span class="sxs-lookup"><span data-stu-id="03f23-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="03f23-122">Por ejemplo, mediante \[A Z\] en *modelo* da como resultado una coincidencia si la posición del carácter correspondiente en *expresión* contiene cualquiera de las letras mayúsculas en el intervalo de la a la Z. Puede incluir varios intervalos dentro de los corchetes sin delimitar los intervalos.</span><span class="sxs-lookup"><span data-stu-id="03f23-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="03f23-123">Por ejemplo, \[a-zA-Z0-9\] coincide con cualquier carácter alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="03f23-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="03f23-124">Es importante tener en cuenta que los caracteres comodín de ANSI SQL (%) y (\_) sólo están disponibles con Microsoft® Jet versión 4.X y el proveedor Microsoft OLE DB para Jet.</span><span class="sxs-lookup"><span data-stu-id="03f23-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft® Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="03f23-125">Se tratarán como literales si se usan en Microsoft Access o DAO.</span><span class="sxs-lookup"><span data-stu-id="03f23-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="03f23-126">Otras reglas importantes de la coincidencia de patrones son:</span><span class="sxs-lookup"><span data-stu-id="03f23-126">Other important rules for pattern matching include the following:</span></span>

  - <span data-ttu-id="03f23-127">Un signo de exclamación (\!) al principio de *listacaracteres* significa que se realiza una coincidencia si cualquier carácter excepto incluido en *listaDeCaracteres* se encuentra en la *expresión*.</span><span class="sxs-lookup"><span data-stu-id="03f23-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="03f23-128">Si se usa fuera de los corchetes, el signo de exclamación se corresponde consigo mismo.</span><span class="sxs-lookup"><span data-stu-id="03f23-128">When used outside brackets, the exclamation mark matches itself.</span></span>

  - <span data-ttu-id="03f23-129">Puede usar el guión (-) al principio (después de un signo de exclamación si se utiliza uno) o al final de *listacaracteres* para que coincida con el propio.</span><span class="sxs-lookup"><span data-stu-id="03f23-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="03f23-130">En cualquier otra posición, el guión identifica un intervalo de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="03f23-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

  - <span data-ttu-id="03f23-131">Cuando se especifica un intervalo de caracteres, éstos deben aparecer en un criterio de ordenación ascendente (A-Z o 0-100).</span><span class="sxs-lookup"><span data-stu-id="03f23-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="03f23-132">\[A-z\] es un patrón válido, pero \[Z-A\] no es.</span><span class="sxs-lookup"><span data-stu-id="03f23-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

  - <span data-ttu-id="03f23-133">La secuencia de caracteres \[ \] se omite; se considera una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="03f23-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

