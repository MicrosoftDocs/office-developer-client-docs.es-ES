---
title: Método SkipLine (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314563"
---
# <a name="skipline-method-ado"></a>Método SkipLine (ADO)


**Se aplica a:** Access 2013, Office 2013

Omite una línea completa al leer una secuencia de texto.

## <a name="syntax"></a>Sintaxis

*Stream*. SkipLine

## <a name="remarks"></a>Comentarios

Se omiten todos los caracteres hasta el siguiente separador de línea, incluido éste. De manera predeterminada, el valor de [LineSeparator](lineseparator-property-ado.md) es **adCRLF**. Si se intenta omitir caracteres situados más allá de [EOS](eos-property-ado.md), la posición actual se mantendrá simplemente en **EOS**.

El método **SkipLine** se utiliza con secuencias de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**).

