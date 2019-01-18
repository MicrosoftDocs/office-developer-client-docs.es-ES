---
title: Database.Close (método) (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699980"
---
# <a name="databaseclose-method-dao"></a>Database.Close (método) (DAO)


**Se aplica a**: Access 2013, Office 2013

Cierra un objeto **Database** abierto.

## <a name="syntax"></a>Sintaxis

*expresión* . Cerrar

*expresión* Variable que representa un objeto de **base de datos** .

## <a name="remarks"></a>Observaciones

Si el objeto **Database** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.

Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).

