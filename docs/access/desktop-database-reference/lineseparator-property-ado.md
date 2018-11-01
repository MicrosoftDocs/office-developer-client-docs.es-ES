---
title: LineSeparator (propiedad, ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 831b6377ade43b3be04ed21add20fbd10e48ac2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882507"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="39699-102">LineSeparator (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="39699-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="39699-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39699-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39699-104">Indica el carácter binario que se utiliza como separador de línea en objetos de texto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="39699-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="39699-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="39699-105">Settings and return values</span></span>

<span data-ttu-id="39699-p101">Establece o devuelve un valor de tipo [LineSeparatorsEnum](lineseparatorsenum.md) que indica el carácter separador de línea utilizado en el objeto **Stream**. El valor predeterminado es **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="39699-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="39699-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39699-108">Remarks</span></span>

<span data-ttu-id="39699-p102">**LineSeparator** se utiliza para interpretar líneas al leer el contenido de un objeto de texto **Stream**. Las líneas se pueden omitir con el método [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="39699-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="39699-p103">**LineSeparator** sólo se utiliza con objetos de texto **Stream** ([Type](type-property-ado-stream.md) es **adTypeText**). Esta propiedad se pasa por alto si **Type** es **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="39699-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

