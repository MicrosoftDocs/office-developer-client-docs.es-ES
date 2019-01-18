---
title: EOS (propiedad, ADO - referencia de escritorio de la base de datos de Access))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716603"
---
# <a name="eos-property-ado"></a><span data-ttu-id="e9aa6-102">EOS (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="e9aa6-102">EOS property (ADO)</span></span>


<span data-ttu-id="e9aa6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9aa6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9aa6-104">Indica si la posición actual se encuentra al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e9aa6-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9aa6-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e9aa6-105">Return values</span></span>

<span data-ttu-id="e9aa6-p101">Devuelve un valor de tipo **Boolean** que indica si la posición actual se encuentra al final de la secuencia. **EOS** devuelve **True** si no hay más bytes en la secuencia y **False** si hay más bytes detrás de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="e9aa6-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="e9aa6-p102">Para establecer el fin de la secuencia, utilice el método [SetEOS](seteos-method-ado.md). Para determinar la posición actual, utilice la propiedad [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e9aa6-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

