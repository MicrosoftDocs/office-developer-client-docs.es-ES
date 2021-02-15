---
title: Propiedad Recordset.CacheStart (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300619"
---
# <a name="recordsetcachestart-property-dao"></a>Propiedad Recordset.CacheStart (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que especifica el marcador del primer registro en un objeto Recordset de tipo Dynaset que contiene datos para almacenar en la memoria caché localmente desde un origen de datos ODBC (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . CacheStart

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

El almacenamiento en la memoria caché de datos mejora el rendimiento si se usan objetos **Recordset** para recuperar datos de un servidor remoto. Una memoria caché es un espacio en la memoria local que contiene los datos recuperados más recientemente en el servidor; esto es útil si los usuarios solicitan los datos de nuevo mientras se ejecuta la aplicación. Cuando los usuarios solicitan datos, el motor de base de datos de Microsoft Access busca primero en la memoria caché los datos solicitados en lugar de recuperarlos del servidor, que requiere más tiempo. En la memoria caché solo se guardan los datos procedentes de un origen de datos ODBC.

Cualquier motor de base de datos de Microsoft Access conectado a un origen de datos ODBC como, por ejemplo, una tabla vinculada, puede tener una caché local. Para crear una memoria caché, abra un objeto **Recordset** de un origen de datos remoto, establezca las propiedades **CacheSize** y **[CacheStart](recordset-cachestart-property-dao.md)** y, a continuación, use el método **[FillCache](recordset-fillcache-method-dao.md)** o examine los registros usando los métodos **Move**.

El valor de la propiedad **CacheStart** es el marcador del primer registro del objeto **Recordset** que se va a almacenar en la memoria caché. Puede usar el marcador de un registro para establecer la propiedad **CacheStart**. Convierta el registro que desee que comience la memoria caché en el registro actual y establezca la propiedad **CacheStart** con el mismo valor que la propiedad **[Bookmark](recordset-bookmark-property-dao.md)**.

El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché desde la caché y solicita registros fuera del intervalo de caché desde el servidor.

Los registros recuperados de la caché no reflejan los cambios realizados simultáneamente por otros usuarios en los datos del origen.

Para forzar una actualización de todos los datos almacenados en la memoria caché, establezca la propiedad **CacheSize** del objeto **Recordset** en 0, restablézcala al tamaño de la memoria caché que solicitó originalmente y, finalmente, use el método **FillCache**.

