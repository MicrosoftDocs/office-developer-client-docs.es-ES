---
title: LineSeparator (propiedad, ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289952"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="4be6a-102">LineSeparator (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4be6a-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="4be6a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4be6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4be6a-104">Indica el carácter binario que se utiliza como separador de línea en objetos de texto [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4be6a-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4be6a-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="4be6a-105">Settings and return values</span></span>

<span data-ttu-id="4be6a-106">Establece o devuelve un valor de tipo [LineSeparatorsEnum](lineseparatorsenum.md) que indica el carácter separador de línea utilizado en el objeto **Stream**.</span><span class="sxs-lookup"><span data-stu-id="4be6a-106">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="4be6a-107">El valor predeterminado es **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="4be6a-107">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4be6a-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4be6a-108">Remarks</span></span>

<span data-ttu-id="4be6a-p102">**LineSeparator** se utiliza para interpretar líneas al leer el contenido de un objeto de texto **Stream**. Las líneas se pueden omitir con el método [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4be6a-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="4be6a-111">**LineSeparator** sólo se utiliza con objetos de texto **Stream** ([Type](type-property-ado-stream.md) es **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="4be6a-111">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="4be6a-112">Esta propiedad se pasa por alto si **Type** es **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="4be6a-112">This property is ignored if **Type** is **adTypeBinary**.</span></span>

