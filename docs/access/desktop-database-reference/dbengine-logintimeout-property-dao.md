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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294312"
---
# <a name="dbenginelogintimeout-property-dao"></a>Propiedad DBEngine.LoginTimeout (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . LoginTimeout

*expression* Variable que representa un objeto **DBEngine**.

## <a name="remarks"></a>Comentarios

La propiedad predeterminada **LoginTimeout** está configurada en 20 segundos. Cuando la propiedad **LoginTimeout** está configurada en 0, no se produce tiempo de espera.

Si está intentando conectarse a una base de datos ODBC como, por ejemplo, Microsoft SQL Server, puede producirse un error en la conexión como resultado de errores de red o porque el servidor está apagado. Mejor que esperar los 20 segundos predeterminados para realizar la conexión, puede especificar el tiempo de espera antes de que aparezca un error. Una conexión al servidor se produce implícitamente como parte de diferentes eventos, tales como ejecutar una consulta o conectarse a un servidor de base de datos externo.

