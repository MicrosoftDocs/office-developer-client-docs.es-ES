---
title: DBEngine.DefaultPassword Property (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a418d10773326e36f5c7111cce5941fb7255cb89
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861206"
---
# <a name="dbenginedefaultpassword-property-dao"></a>DBEngine.DefaultPassword Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece la contraseña utilizada para crear el objeto **Workspace** predeterminado cuando se inicializa. **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . DefaultPassword

*expresión* Variable que representa un objeto **DBEngine** .

## <a name="remarks"></a>Observaciones

El valor de **DefaultPassword** es un tipo de datos String que puede tener una longitud de hasta 20 caracteres. Puede contener cualquier carácter excepto ASCII 0.


> [!NOTE]
> [!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.

De forma predeterminada, la propiedad **DefaultUser** está establecida en "admin" y la propiedad **DefaultPassword** está establecida en una cadena de longitud cero ("").

En general, se utiliza el método **CreateWorkspace** para crear un objeto **Workspace** con un nombre de usuario y una contraseña determinados. Sin embargo, por compatibilidad con versiones anteriores y por comodidad cuando no se implementa una base de datos protegida, el motor de base de datos de Microsoft Access crea automáticamente un objeto **Workspace** predeterminado cuando es necesario si no hay uno abierto. En este caso, los valores de las propiedades **DefaultUser** y **DefaultPassword** definen el nombre de usuario y la contraseña para el objeto **Workspace** predeterminado.

Para que esta propiedad surta efecto, debe establecerla antes de llamar a los métodos DAO.

