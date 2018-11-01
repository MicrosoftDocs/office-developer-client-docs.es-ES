---
title: Busque el método - ActiveX Data Objects (ADO)
TOCTitle: Find Method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929e4ac695ff65c3576f2ffb8ad1baf8ab1d1137
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870628"
---
# <a name="find-method-ado"></a><span data-ttu-id="6f981-102">Find (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="6f981-102">Find Method (ADO)</span></span>


<span data-ttu-id="6f981-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f981-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6f981-p101">Busca en un objeto [Recordset](recordset-object-ado.md) la fila que cumpla los criterios especificados. De manera opcional, se puede especificar la dirección de la búsqueda, la fila inicial y el desplazamiento desde la fila inicial. Si se cumplen los criterios, la posición de fila actual se establece en el registro encontrado; en caso contrario, se establece en el final (o el inicio) del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6f981-p101">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f981-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f981-107">Syntax</span></span>

<span data-ttu-id="6f981-108">Buscar (*criterios*, *SkipRows*, *SearchDirection*, *Iniciar*)</span><span class="sxs-lookup"><span data-stu-id="6f981-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6f981-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f981-109">Parameters</span></span>

  - <span data-ttu-id="6f981-110">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="6f981-110">*Criteria*</span></span>

  - <span data-ttu-id="6f981-111">Valor de tipo **String** con una instrucción que especifica el nombre de columna, el operador de comparación y el valor que se van a utilizar en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6f981-111">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>

  - <span data-ttu-id="6f981-112">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="6f981-112">*SkipRows*</span></span>

  - <span data-ttu-id="6f981-p102">Es opcional *.* Valor de tipo **Long**, cuyo valor predeterminado es cero, que especifica el desplazamiento con respecto a la fila actual o el marcador *Start* para iniciar la búsqueda. De forma predeterminada, la búsqueda inicia en la fila actual.</span><span class="sxs-lookup"><span data-stu-id="6f981-p102">Optional *.* A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search. By default, the search will start on the current row.</span></span>

  - <span data-ttu-id="6f981-116">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="6f981-116">*SearchDirection*</span></span>

  - <span data-ttu-id="6f981-p103">Es opcional *.* Valor de [SearchDirectionEnum](searchdirectionenum.md) que especifica si la búsqueda debe iniciar en la fila actual o la siguiente fila disponible en dirección de la búsqueda. Una búsqueda sin resultados se detiene al final del objeto **Recordset** si el valor es **adSearchForward**. Una búsqueda sin resultados se detiene al principio del objeto **Recordset** si el valor es **adSearchBackward**.</span><span class="sxs-lookup"><span data-stu-id="6f981-p103">Optional *.* A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search. An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**. An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>

  - <span data-ttu-id="6f981-121">*Start*</span><span class="sxs-lookup"><span data-stu-id="6f981-121">*Start*</span></span>

  - <span data-ttu-id="6f981-p104">Es opcional. Marcador de tipo **Variant** que funciona como posición inicial de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6f981-p104">Optional. A **Variant** bookmark that functions as the starting position for the search.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f981-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f981-124">Remarks</span></span>

<span data-ttu-id="6f981-p105">Se puede especificar únicamente el nombre de una sola columna en *Criteria*. Este método no admite búsquedas en varias columnas.</span><span class="sxs-lookup"><span data-stu-id="6f981-p105">Only a single-column name may be specified in *criteria*. This method does not support multi-column searches.</span></span>

<span data-ttu-id="6f981-127">Es posible que el operador de comparación en *Criteria* "**\>**"(mayor que),"**\<**"(menor que), "=" (igual a),"\>=" (mayor o igual que), "\<=" (menor o igual que), "\<\>" (no igual a), o "like" (coincidencia de modelos).</span><span class="sxs-lookup"><span data-stu-id="6f981-127">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="6f981-128">El valor especificado en *Criteria* puede ser una cadena, un número de punto flotante o una fecha.</span><span class="sxs-lookup"><span data-stu-id="6f981-128">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="6f981-129">Valores de cadena se delimitan con comillas simples o "\#" (signo de número) marca (por ejemplo, "estado = 'WA'" o "estado = \#WA\#").</span><span class="sxs-lookup"><span data-stu-id="6f981-129">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="6f981-130">Los valores de fecha se delimitan con "\#" (signo de número) marca (por ejemplo, "iniciar\_fecha \> \#22/7/97\#") y pueden contener horas, minutos y segundos para indicar las marcas de tiempo pero no deben contener milisegundos o se producirán errores .</span><span class="sxs-lookup"><span data-stu-id="6f981-130">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="6f981-p107">Si el operador de comparación es "like", el valor de cadena puede contener un asterisco (\*) para que se busque una o varias apariciones de cualquier carácter o subcadena. Por ejemplo, "state like 'M\*'" encuentra Maine y Massachusetts. También se pueden utilizar asteriscos inicial y final para buscar una subcadena incluida en los valores. Por ejemplo, "state like '\*as\*' encuentra Alaska, Arkansas y Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="6f981-p107">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="6f981-p108">Se pueden utilizar asteriscos sólo al final de la cadena, o bien, tanto al principio como al final de la cadena, tal y como se ha mostrado anteriormente. No se puede utilizar el asterisco como comodín inicial ('\*str') o comodín incrustado ('s\*r'). En caso contrario, se provocará un error.</span><span class="sxs-lookup"><span data-stu-id="6f981-p108">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r'). This will cause an error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6f981-p109">[!NOTA] Se producirá un error si no se establece una posición de fila actual antes de llamar a <STRONG>Find</STRONG>. Es preciso llamar a algún método que establezca la posición de fila, como el método <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, antes de llamar a <STRONG>Find</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6f981-p109">An error will occur if a current row position is not set before calling <STRONG>Find</STRONG>. Any method that sets row position, such as <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, should be called before calling <STRONG>Find</STRONG>.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="6f981-p110">[!NOTA] Si llama al método <STRONG>Find</STRONG> en un conjunto de registros y la posición actual en el conjunto de registros se encuentra en el último registro o al final del archivo (EOF), la búsqueda no tendrá resultados. Deberá llamar al método <STRONG>MoveFirst</STRONG> para establecer el cursor o la posición actual en el inicio del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="6f981-p110">If you call the <STRONG>Find</STRONG> method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything. You need to call the <STRONG>MoveFirst</STRONG> method to set the current position/cursor to the beginning of the recordset.</span></span></P>


