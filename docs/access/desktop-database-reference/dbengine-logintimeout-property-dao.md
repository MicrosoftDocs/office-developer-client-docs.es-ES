---
title: Propiedad DBEngine.LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e3ff893a16e650fe7eb49b647ae8d67374375a0d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701931"
---
# <a name="dbenginelogintimeout-property-dao"></a>Propiedad DBEngine.LoginTimeout (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . LoginTimeout

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="remarks"></a>Observaciones

El valor predeterminado de la propiedad **LoginTimeout** es de 20 segundos. Cuando la propiedad **LoginTimeout** se establece en 0, no se produce tiempo de espera.

Cuando se intenta establecer sesión en una base de datos ODBC, como Microsoft SQL Server, puede producirse un error en la conexión debido a errores en la red o a que el servidor no esté funcionando. En lugar de esperar los 20 segundos predeterminados para establecer la conexión, se puede especificar cuánto tiempo se desea esperar antes de que se produzca un error. El inicio de sesión en el servidor se produce implícitamente como parte de una serie de eventos diferentes, como la ejecución de una consulta en una base de datos externa del servidor.

