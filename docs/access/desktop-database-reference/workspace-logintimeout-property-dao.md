---
title: Propiedad Workspace.LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07b2945f2e9a59cc8a7db4a6f5a44cfaf9b35043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928288"
---
# <a name="workspacelogintimeout-property-dao"></a>Propiedad Workspace.LoginTimeout (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . LoginTimeout

*expresión* Variable que representa un objeto **Workspace** .

## <a name="remarks"></a>Observaciones

El valor predeterminado de la propiedad **LoginTimeout** es de 20 segundos. Cuando la propiedad **LoginTimeout** se establece en 0, no se produce tiempo de espera.

Cuando se intenta establecer sesión en una base de datos ODBC, como Microsoft SQL Server, puede producirse un error en la conexión debido a errores en la red o a que el servidor no esté funcionando. En lugar de esperar los 20 segundos predeterminados para establecer la conexión, se puede especificar cuánto tiempo se desea esperar antes de que se produzca un error. El inicio de sesión en el servidor se produce implícitamente como parte de una serie de eventos diferentes, como la ejecución de una consulta en una base de datos externa del servidor.

