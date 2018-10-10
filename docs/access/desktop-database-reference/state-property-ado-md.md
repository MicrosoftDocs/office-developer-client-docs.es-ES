---
title: State (propiedad, ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a42ade39a50eb5dc40e213d6f4c3f4ed0ba3475e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484806"
---
# <a name="state-property-ado-md"></a>State (propiedad, ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Indica el estado actual del conjunto de celdas.

## <a name="return-values"></a>Valores devueltos

Devuelve un entero **Long** que indica el estado actual del objeto [Cellset](cellset-object-ado-md.md) y es de sólo lectura. Los valores siguientes son válidos: **adStateClosed** (0) y **adStateOpen** (1).

## <a name="remarks"></a>Comentarios

Para usar los nombres de constantes [ObjectStateEnum](objectstateenum.md), debe existir una referencia a la biblioteca de tipos ADO en su proyecto. Vea [Utilizar ADO con ADO MD](using-ado-with-ado-md.md) para obtener más información.

