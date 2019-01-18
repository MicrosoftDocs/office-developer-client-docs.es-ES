---
title: SetEOS (método, ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f3b1ee81928a8da77cc3edff7f1feffb7196bba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722763"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="cce7a-102">SetEOS (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="cce7a-102">SetEOS method (ADO)</span></span>

<span data-ttu-id="cce7a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cce7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cce7a-104">Establece la posición que es el final de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cce7a-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cce7a-105">Syntax</span></span>

<span data-ttu-id="cce7a-106">*Secuencia*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="cce7a-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="cce7a-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cce7a-107">Remarks</span></span>

<span data-ttu-id="cce7a-p101">**SetEOS** actualiza el valor de la propiedad [EOS](eos-property-ado.md), convirtiendo el valor actual de [Position](position-property-ado.md) en el final de la secuencia. Los bytes o caracteres situados después de la posición actual se truncan.</span><span class="sxs-lookup"><span data-stu-id="cce7a-p101">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream. Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="cce7a-110">Dado que [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) y [CopyTo](copyto-method-ado.md) no truncan los valores adicionales en los objetos **Stream** existentes, se pueden truncar estos bytes o caracteres estableciendo la nueva posición de final de secuencia con **SetEOS**.</span><span class="sxs-lookup"><span data-stu-id="cce7a-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>

> [!WARNING]
> <span data-ttu-id="cce7a-111">Si se establece el valor de **EOS** en una posición situada delante del final real de la secuencia, se perderán todos los datos que se encuentren después de la nueva posición **EOS**.</span><span class="sxs-lookup"><span data-stu-id="cce7a-111">If you set **EOS** to a position before the actual end of the stream, you will lose all data after the new **EOS** position.</span></span>
