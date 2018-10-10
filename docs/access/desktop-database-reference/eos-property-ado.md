---
title: EOS (propiedad, ADO - referencia de escritorio de la base de datos de Access))
TOCTitle: EOS Property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4c6d96e2c143cb0548a2de987f11ea708d1669a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484943"
---
# <a name="eos-property-ado"></a><span data-ttu-id="4e5e9-102">EOS (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="4e5e9-102">EOS Property (ADO)</span></span>


<span data-ttu-id="4e5e9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e5e9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4e5e9-104">Indica si la posición actual se encuentra al final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="4e5e9-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="4e5e9-105">Return Values</span></span>

<span data-ttu-id="4e5e9-p101">Devuelve un valor de tipo **Boolean** que indica si la posición actual se encuentra al final de la secuencia. **EOS** devuelve **True** si no hay más bytes en la secuencia y **False** si hay más bytes detrás de la posición actual.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="4e5e9-p102">Para establecer el fin de la secuencia, utilice el método [SetEOS](seteos-method-ado.md). Para determinar la posición actual, utilice la propiedad [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4e5e9-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

