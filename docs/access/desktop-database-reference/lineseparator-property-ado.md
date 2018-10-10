---
title: LineSeparator (propiedad, ADO)
TOCTitle: LineSeparator Property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1aee67410e2abf921bdbd61e6cd8573e090fafd9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485332"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="77249-102">LineSeparator (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="77249-102">LineSeparator Property (ADO)</span></span>


<span data-ttu-id="77249-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="77249-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="77249-104">Indica el carácter binario que se utiliza como separador de línea en objetos de texto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="77249-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="77249-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="77249-105">Settings and Return Values</span></span>

<span data-ttu-id="77249-p101">Establece o devuelve un valor de tipo [LineSeparatorsEnum](lineseparatorsenum.md) que indica el carácter separador de línea utilizado en el objeto **Stream**. El valor predeterminado es **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="77249-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="77249-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77249-108">Remarks</span></span>

<span data-ttu-id="77249-p102">**LineSeparator** se utiliza para interpretar líneas al leer el contenido de un objeto de texto **Stream**. Las líneas se pueden omitir con el método [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="77249-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="77249-p103">**LineSeparator** sólo se utiliza con objetos de texto **Stream** ([Type](type-property-ado-stream.md) es **adTypeText**). Esta propiedad se pasa por alto si **Type** es **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="77249-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

