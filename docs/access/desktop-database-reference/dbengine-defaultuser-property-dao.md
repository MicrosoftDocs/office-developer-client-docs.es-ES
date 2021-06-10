---
title: Propiedad DBEngine.DefaultUser (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294353"
---
# <a name="dbenginedefaultuser-property-dao"></a>Propiedad DBEngine.DefaultUser (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece el nombre de usuario utilizado para crear el objeto **Workspace** predeterminado cuando se inicializa. **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . DefaultUser

*expression* Expresión que devuelve un objeto **DBEngine**.

## <a name="remarks"></a>Comentarios

El valor de **DefaultUser** es un tipo de datos String. Puede tener entre 1 y 20 caracteres en áreas de trabajo de Microsoft Access y puede incluir caracteres alfabéticos, caracteres acentuados, números, espacios y símbolos excepto: " (comillas), / (barra diagonal hacia \\ delante), (barras diagonal inversa), \[ \] (corchetes), : (dos puntos), | (pipe), \< (menor que sign), \> (mayor que sign), + (signo más), = (signo igual), ; (punto y coma), , ( coma), ? (signo de \* interrogación), (asterisco), espacios iniciales y caracteres de control (ASCII 00 a ASCII 31).


> [!NOTE]
> [!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.

De forma predeterminada, la propiedad **DefaultUser** está establecida en "admin" y la propiedad **DefaultPassword** está establecida en una cadena de longitud cero ("").

Los nombres de usuario no suelen distinguir entre mayúsculas y minúsculas; sin embargo, si va a volver a crear una cuenta de usuario que se ha eliminado o creado en un grupo de trabajo diferente, el nombre de usuario debe coincidir exactamente en las mayúsculas y minúsculas con el nombre original. Las contraseñas sí distinguen entre mayúsculas y minúsculas.

En general, se utiliza el método **CreateWorkspace** para crear un objeto **Workspace** con un nombre de usuario y una contraseña determinados. Sin embargo, por compatibilidad con versiones anteriores y por comodidad cuando no se implementa una base de datos protegida, el motor de base de datos de Microsoft Access crea automáticamente un objeto **Workspace** predeterminado cuando es necesario si no hay uno abierto. En este caso, los valores de las propiedades **DefaultUser** y **DefaultPassword** definen el nombre de usuario y la contraseña para el objeto **Workspace** predeterminado.

Para que esta propiedad surta efecto, debe establecerla antes de llamar a los métodos DAO.

