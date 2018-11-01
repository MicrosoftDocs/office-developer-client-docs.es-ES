---
title: TableDef.ConflictTable Property (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 81b7793291575ca86b5eec628ac9472a20d90ce4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870663"
---
# <a name="tabledefconflicttable-property-dao"></a>TableDef.ConflictTable Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Devuelve el nombre de una tabla de conflictos que contiene los registros de base de datos que generaron conflictos durante la sincronización de dos réplicas (sólo áreas de trabajo de Microsoft Access). **String** de sólo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . ConflictTable

*expresión* Expresión que devuelve un objeto **TableDef** .

## <a name="remarks"></a>Observaciones

El valor devuelto es un tipo de datos **String** que es una cadena de longitud cero ("") si no hay ninguna tabla de conflictos o la base de datos no es una réplica.

Si dos usuarios en dos réplicas independientes realizan cada uno un cambio en el mismo registro de la base de datos, los cambios efectuados por uno de los usuarios no se aplicarán en la otra réplica. En consecuencia, el usuario cuyos cambios no se aplicaron debe resolver los conflictos.

Los conflictos se producen en el nivel de registro, no entre campos. Por ejemplo, si un usuario cambia el campo Dirección y otro actualiza el campo Teléfono del mismo registro, uno de los cambios se rechaza. Puesto que los conflictos se producen en el nivel de registro, el rechazo se produce incluso si es improbable que el cambio realizado y el cambio rechazado den como resultado un conflicto real de información.

El mecanismo de sincronización controla los conflictos de registros mediante la creación de tablas de conflictos, que contienen la información que se habría incluido en la tabla si el cambio hubiera tenido éxito. Puede examinar estas tablas de conflictos fila por fila para realizar las correcciones correspondientes.

Todas las tablas de conflictos se denominan tabla\_conflicto, donde tabla es el nombre original de la tabla, truncado a la longitud del nombre de tabla máximo.

