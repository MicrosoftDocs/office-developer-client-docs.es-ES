---
title: Propiedad DBEngine.IniPath (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717632"
---
# <a name="dbengineinipath-property-dao"></a>Propiedad DBEngine.IniPath (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve información sobre la clave del Registro de Windows que contiene los valores para el motor de base de datos Microsoft Access (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . IniPath

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="remarks"></a>Observaciones

Puede configurar el motor de base de datos de Microsoft Access con el registro de Windows. Puede utilizar el Registro para configurar opciones, tales como los archivos DLL de un archivo ISAM instalable.

Para que esta opción funcione, debe establecer la propiedad **IniPath** antes de que su aplicación llame a cualquier otro código DAO. El ámbito de esta configuración está limitado a la aplicación y no se puede cambiar sin reiniciar ésta.

Utilice también el Registro para proporcionar parámetros de inicialización para algunos controladores de base de datos ISAM instalables. Por ejemplo, para utilizar la versión 4.0 de Paradox, establezca la propiedad **IniPath** como parte del Registro con los parámetros apropiados.

Esta propiedad reconoce alguno HKEY\_LOCAL\_máquina o HKEY\_LOCAL\_usuario. Si no hay ninguna clave de raíz se proporciona, el valor predeterminado es HKEY\_LOCAL\_máquina.

