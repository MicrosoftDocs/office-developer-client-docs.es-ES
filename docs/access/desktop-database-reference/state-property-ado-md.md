---
title: State (propiedad, ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702449"
---
# <a name="state-property-ado-md"></a>State (propiedad, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Indica el estado actual del conjunto de celdas.

## <a name="return-values"></a>Valores devueltos

Devuelve un entero **Long** que indica el estado actual del objeto [Cellset](cellset-object-ado-md.md) y es de sólo lectura. Los valores siguientes son válidos: **adStateClosed** (0) y **adStateOpen** (1).

## <a name="remarks"></a>Comentarios

Para usar los nombres de constantes [ObjectStateEnum](objectstateenum.md), debe existir una referencia a la biblioteca de tipos ADO en su proyecto. Vea [Utilizar ADO con ADO MD](using-ado-with-ado-md.md) para obtener más información.

