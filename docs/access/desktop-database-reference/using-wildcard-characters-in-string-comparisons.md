---
title: Uso de caracteres comodín en comparaciones de cadenas
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305939"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="3baf3-102">Uso de caracteres comodín en comparaciones de cadenas</span><span class="sxs-lookup"><span data-stu-id="3baf3-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="3baf3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3baf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3baf3-p101">La coincidencia de patrones integrada proporciona una herramienta versátil para realizar comparaciones de cadenas. En la siguiente tabla, se muestran los caracteres comodín que puede usar con el operador **Like** y el número de dígitos o cadenas con los que se corresponden.</span><span class="sxs-lookup"><span data-stu-id="3baf3-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3baf3-106">Caracteres en <em>patrón</em></span><span class="sxs-lookup"><span data-stu-id="3baf3-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="3baf3-107">Correspondencia en <em>expresión</em></span><span class="sxs-lookup"><span data-stu-id="3baf3-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3baf3-p102">? o _ (subrayado)</span><span class="sxs-lookup"><span data-stu-id="3baf3-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="3baf3-110">Cualquier carácter</span><span class="sxs-lookup"><span data-stu-id="3baf3-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3baf3-111">\* o %</span><span class="sxs-lookup"><span data-stu-id="3baf3-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="3baf3-112">Cero o más caracteres</span><span class="sxs-lookup"><span data-stu-id="3baf3-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="3baf3-113">Un único dígito (0 – 9)</span><span class="sxs-lookup"><span data-stu-id="3baf3-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3baf3-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="3baf3-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="3baf3-115">Cualquier carácter de <em>listaDeCaracteres</em></span><span class="sxs-lookup"><span data-stu-id="3baf3-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3baf3-116">[! <em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="3baf3-116">[!<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="3baf3-117">Un único carácter no incluido en <em>listaDeCaracteres</em></span><span class="sxs-lookup"><span data-stu-id="3baf3-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3baf3-118">Puede usar un grupo de uno o varios caracteres (*charlist*) entre corchetes ( ) para coincidir con cualquier carácter individual de la expresión, y charlist puede incluir casi cualquier carácter en el conjunto de caracteres ANSI, incluidos los \[ \] dígitos.  </span><span class="sxs-lookup"><span data-stu-id="3baf3-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="3baf3-119">Puede usar el corchete de apertura de caracteres especiales ( ), signo de interrogación (?), signo de número ( ) y asterisco ( ) para que coincidan directamente solo si están entre \[ \# \* corchetes.</span><span class="sxs-lookup"><span data-stu-id="3baf3-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="3baf3-120">No puede usar el corchete de cierre ( ) dentro de un grupo para que coincida con sí mismo, pero puede usarlo fuera de un \] grupo como un carácter individual.</span><span class="sxs-lookup"><span data-stu-id="3baf3-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="3baf3-121">Además de una lista simple de caracteres incluidos entre corchetes, *listaDeCaracteres* puede especificar un intervalo de caracteres utilizando un guión (-) para separar los límites inicial y final del intervalo.</span><span class="sxs-lookup"><span data-stu-id="3baf3-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="3baf3-122">Por ejemplo, el uso de A-Z en el patrón da como resultado una coincidencia si la posición de carácter correspondiente en la expresión contiene alguna de las letras mayúsculas del intervalo \[ \] A a Z.   Puede incluir varios intervalos entre corchetes sin delimitar los intervalos.</span><span class="sxs-lookup"><span data-stu-id="3baf3-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="3baf3-123">Por ejemplo, \[ a-zA-Z0-9 \] coincide con cualquier carácter alfanumérico.</span><span class="sxs-lookup"><span data-stu-id="3baf3-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="3baf3-124">Es importante tener en cuenta que ansi SQL caracteres comodín (%) and ( \_ ) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span><span class="sxs-lookup"><span data-stu-id="3baf3-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="3baf3-125">Se tratarán como literales si se usan en Microsoft Access o DAO.</span><span class="sxs-lookup"><span data-stu-id="3baf3-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="3baf3-126">Otras reglas importantes de la coincidencia de patrones son:</span><span class="sxs-lookup"><span data-stu-id="3baf3-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="3baf3-127">Un signo de exclamación ( ) al principio de charlist significa que se realiza una coincidencia si se encuentra algún carácter excepto los de \! *charlist* en la *expresión*. </span><span class="sxs-lookup"><span data-stu-id="3baf3-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="3baf3-128">Si se usa fuera de los corchetes, el signo de exclamación se corresponde consigo mismo.</span><span class="sxs-lookup"><span data-stu-id="3baf3-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="3baf3-p107">Puede usar el guión (-) al principio (a continuación de un signo de exclamación si se utiliza) o al final de *listaDeCaracteres* en correspondencia consigo mismo. En cualquier otra posición, el guión identifica un intervalo de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="3baf3-p107">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself. In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="3baf3-131">Cuando se especifica un intervalo de caracteres, éstos deben aparecer en un criterio de ordenación ascendente (A-Z o 0-100).</span><span class="sxs-lookup"><span data-stu-id="3baf3-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="3baf3-132">\[A-Z \] es un patrón válido, pero \[ Z-A \] no lo es.</span><span class="sxs-lookup"><span data-stu-id="3baf3-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="3baf3-133">La secuencia de caracteres se omite; se considera una cadena de \[ \] longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="3baf3-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

