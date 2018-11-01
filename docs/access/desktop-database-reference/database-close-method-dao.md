---
title: Database.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92b4075f09bb34eca465f49d30a9ba8777b3e583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869655"
---
# <a name="databaseclose-method-dao"></a>Database.Close Method (DAO)


**Se aplica a**: Access 2013, Office 2013

Cierra un objeto **Database** abierto.

## <a name="syntax"></a>Sintaxis

*expresión* . Cerrar

*expresión* Variable que representa un objeto de **base de datos** .

## <a name="remarks"></a>Observaciones

Si el objeto **Database** ya está cerrado cuando utiliza **Close**, se produce un error en tiempo de ejecución.

Una alternativa al método **Close** es establecer el valor de una variable de objeto en **Nothing** (Set dbsTemp = Nothing).

