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
# <a name="eos-property-ado"></a>EOS (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica si la posición actual se encuentra al final de la secuencia.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor de tipo **Boolean** que indica si la posición actual se encuentra al final de la secuencia. **EOS** devuelve **True** si no hay más bytes en la secuencia y **False** si hay más bytes detrás de la posición actual.

Para establecer el fin de la secuencia, utilice el método [SetEOS](seteos-method-ado.md). Para determinar la posición actual, utilice la propiedad [Position](position-property-ado.md).

