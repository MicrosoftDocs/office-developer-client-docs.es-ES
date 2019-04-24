---
title: Propiedad DBEngine. DefaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294361"
---
# <a name="dbenginedefaultpassword-property-dao"></a>Propiedad DBEngine. DefaultPassword (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece la contraseña utilizada para crear el objeto **Workspace** predeterminado cuando se inicializa. **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . DefaultPassword

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="remarks"></a>Comentarios

El valor de **DefaultPassword** es un tipo de datos String que puede tener una longitud de hasta 20 caracteres. Puede contener cualquier carácter excepto ASCII 0.


> [!NOTE]
> [!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.

De forma predeterminada, la propiedad **DefaultUser** está establecida en "admin" y la propiedad **DefaultPassword** está establecida en una cadena de longitud cero ("").

En general, se utiliza el método **CreateWorkspace** para crear un objeto **Workspace** con un nombre de usuario y una contraseña determinados. Sin embargo, por compatibilidad con versiones anteriores y por comodidad cuando no se implementa una base de datos protegida, el motor de base de datos de Microsoft Access crea automáticamente un objeto **Workspace** predeterminado cuando es necesario si no hay uno abierto. En este caso, los valores de las propiedades **DefaultUser** y **DefaultPassword** definen el nombre de usuario y la contraseña para el objeto **Workspace** predeterminado.

Para que esta propiedad surta efecto, debe establecerla antes de llamar a los métodos DAO.

