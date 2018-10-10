---
title: Declaración WITH OWNERACCESS OPTION (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)
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
ms.openlocfilehash: b47b9fcc5b3c4422ec60bbdaf06193533c20b6e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486205"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>Declaración WITH OWNERACCESS OPTION (Microsoft Access SQL)


**Se aplica a**: Access 2013 | Office 2013

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

