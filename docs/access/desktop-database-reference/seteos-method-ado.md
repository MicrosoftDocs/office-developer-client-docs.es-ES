---
title: SetEOS (método, ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b45e716844b3e616dfe5b8f94d69f29d6b0f1042
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997514"
---
# <a name="seteos-method-ado"></a>SetEOS (método, ADO)

**Se aplica a**: Access 2013, Office 2013

Establece la posición que es el final de la secuencia.

## <a name="syntax"></a>Sintaxis

*Secuencia*. SetEOS

## <a name="remarks"></a>Comentarios

**SetEOS** actualiza el valor de la propiedad [EOS](eos-property-ado.md), convirtiendo el valor actual de [Position](position-property-ado.md) en el final de la secuencia. Los bytes o caracteres situados después de la posición actual se truncan.

Dado que [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) y [CopyTo](copyto-method-ado.md) no truncan los valores adicionales en los objetos **Stream** existentes, se pueden truncar estos bytes o caracteres estableciendo la nueva posición de final de secuencia con **SetEOS**.

> [!WARNING]
> Si se establece el valor de **EOS** en una posición situada delante del final real de la secuencia, se perderán todos los datos que se encuentren después de la nueva posición **EOS**.