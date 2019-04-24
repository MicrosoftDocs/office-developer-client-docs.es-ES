---
title: Propiedad Workspace. LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306912"
---
# <a name="workspacelogintimeout-property-dao"></a>Propiedad Workspace. LoginTimeout (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . LoginTimeout

*expresión* Variable que representa un objeto **Workspace** .

## <a name="remarks"></a>Comentarios

La propiedad predeterminada **LoginTimeout** está configurada en 20 segundos. Cuando la propiedad **LoginTimeout** está configurada en 0, no se produce tiempo de espera.

Si está intentando conectarse a una base de datos ODBC como, por ejemplo, Microsoft SQL Server, puede producirse un error en la conexión como resultado de errores de red o porque el servidor está apagado. Mejor que esperar los 20 segundos predeterminados para realizar la conexión, puede especificar el tiempo de espera antes de que aparezca un error. Una conexión al servidor se produce implícitamente como parte de diferentes eventos, tales como ejecutar una consulta o conectarse a un servidor de base de datos externo.

