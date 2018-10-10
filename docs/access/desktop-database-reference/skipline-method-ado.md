---
title: SkipLine (método, ADO)
TOCTitle: SkipLine Method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28cb222a3ed0e5497e03efbb7394081c96b4d4ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485054"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="52e9d-102">SkipLine (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="52e9d-102">SkipLine Method (ADO)</span></span>


<span data-ttu-id="52e9d-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="52e9d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="52e9d-104">Omite una línea completa al leer una secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="52e9d-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e9d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52e9d-105">Syntax</span></span>

<span data-ttu-id="52e9d-106">*Secuencia*. SkipLine</span><span class="sxs-lookup"><span data-stu-id="52e9d-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="52e9d-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52e9d-107">Remarks</span></span>

<span data-ttu-id="52e9d-p101">Se omiten todos los caracteres hasta el siguiente separador de línea, incluido éste. De manera predeterminada, el valor de [LineSeparator](lineseparator-property-ado.md) es **adCRLF**. Si se intenta omitir caracteres situados más allá de [EOS](eos-property-ado.md), la posición actual se mantendrá simplemente en **EOS**.</span><span class="sxs-lookup"><span data-stu-id="52e9d-p101">All characters up to, and including the next line separator, are skipped. By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**. If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="52e9d-111">El método **SkipLine** se utiliza con secuencias de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="52e9d-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>

