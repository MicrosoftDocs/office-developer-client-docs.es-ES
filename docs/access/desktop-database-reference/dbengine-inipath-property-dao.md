---
title: DBEngine.IniPath (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294298"
---
# <a name="dbengineinipath-property-dao"></a>DBEngine.IniPath (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve información sobre la clave del Registro de Windows que contiene los valores para el motor de base de datos Microsoft Access (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . IniPath

*expression* Variable que representa un objeto **DBEngine**.

## <a name="remarks"></a>Comentarios

Puede configurar el motor de base de datos de Microsoft Access con el Windows registro. Puede utilizar el Registro para configurar opciones, tales como los archivos DLL de un archivo ISAM instalable.

Para que esta opción funcione, debe establecer la propiedad **IniPath** antes de que su aplicación llame a cualquier otro código DAO. El ámbito de esta configuración está limitado a la aplicación y no se puede cambiar sin reiniciar ésta.

Utilice también el Registro para proporcionar parámetros de inicialización para algunos controladores de base de datos ISAM instalables. Por ejemplo, para utilizar la versión 4.0 de Paradox, establezca la propiedad **IniPath** como parte del Registro con los parámetros apropiados.

Esta propiedad reconoce HKEY \_ LOCAL \_ MACHINE o HKEY LOCAL \_ \_ USER. Si no se proporciona ninguna clave raíz, el valor predeterminado es HKEY \_ LOCAL \_ MACHINE.

