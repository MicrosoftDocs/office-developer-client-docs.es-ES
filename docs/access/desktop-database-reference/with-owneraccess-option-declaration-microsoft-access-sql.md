---
title: CON declaración OWNERACCESS OPTION (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0eca4738d07c54b049073aaf5d4b802864761fa5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920602"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>CON declaración OWNERACCESS OPTION (Microsoft Access SQL)


**Se aplica a**: Access 2013, Office 2013

En un entorno multiusuario con un grupo de trabajo seguro, use esta declaración con una consulta para conceder al usuario que ejecuta la consulta los mismos permisos que tiene el propietario de la consulta.

## <a name="syntax"></a>Sintaxis

*instrucciónsql* CON OWNERACCESS OPTION

## <a name="remarks"></a>Comentarios

La declaración WITH OWNERACCESS OPTION es opcional.

En el siguiente ejemplo, se permite al usuario ver información de salarios (incluso si el usuario no tiene permiso para ver la tabla de nóminas Payroll), siempre que el propietario de la consulta tenga dicho permiso:

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

Si de otra manera un usuario tiene prohibido crear una tabla o agregarle datos, puede usar WITH OWNERACCESS OPTION para permitir que el usuario ejecute una consulta de creación de tabla o de datos anexados.

Si desea aplicar la configuración de seguridad de grupo de trabajo y los permisos de los usuarios, no incluya la declaración WITH OWNERACCESS OPTION.

Esta opción requiere que tenga acceso al archivo System.mdw asociado con la base de datos. Sólo es útil en implementaciones multiusuario protegidas.

