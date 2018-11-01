---
title: SetEOS (método, ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 420d614d100ed156b794e92f77df2e7a4180c9fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872434"
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
> <P>Si se establece el valor de <STRONG>EOS</STRONG> en una posición situada delante del final real de la secuencia, se perderán todos los datos que se encuentren después de la nueva posición <STRONG>EOS</STRONG>.</P>


