---
title: Método Recordset2. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307416"
---
# <a name="recordset2cancel-method-dao"></a>Método Recordset2. Cancel (DAO)


**Se aplica a:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . Cancelar

*expresión* Expresión que devuelve un objeto **Recordset2** .

## <a name="remarks"></a>Comentarios

Utilice el método **Cancel** para terminar la ejecución de una llamada al método **Execute** o **OpenConnection** asincrónica (es decir, el método se ha invocado con la opción dbRunAsync). **Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.

