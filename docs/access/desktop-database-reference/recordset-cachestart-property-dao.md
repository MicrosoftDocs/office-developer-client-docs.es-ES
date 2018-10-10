---
title: Recordset.CacheStart Property (DAO)
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
ms.openlocfilehash: 7ded35253f0cea2243076db6a12caeeee22ecd09
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483907"
---
# <a name="recordsetcachestart-property-dao"></a>Recordset.CacheStart Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Establece o devuelve un valor que especifica el marcador del primer registro de un objeto Recordset de tipo Dynaset que contiene datos que se almacenarán en caché localmente de un origen de datos ODBC (solo áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . CacheStart

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

El almacenamiento en la memoria caché de datos mejora el rendimiento si se usan objetos **Recordset** para recuperar datos de un servidor remoto. Una memoria caché es un espacio en la memoria local que contiene los datos recuperados más recientemente en el servidor; esto es útil si los usuarios solicitan los datos de nuevo mientras se ejecuta la aplicación. Cuando los usuarios solicitan datos, el motor de base de datos de Microsoft Access busca primero en la memoria caché los datos solicitados en lugar de recuperarlos del servidor, que requiere más tiempo. En la memoria caché solo se guardan los datos procedentes de un origen de datos ODBC.

Un origen de datos ODBC conectado al motor de base de datos de Microsoft Access, por ejemplo una tabla vinculada, puede tener una memoria caché local. Para crear la memoria caché, abra un objeto **Recordset** en el origen de datos remoto, establezca las propiedades **CacheSize** y **[CacheStart](recordset-cachestart-property-dao.md)**, y use el método **[FillCache](recordset-fillcache-method-dao.md)** o recorra los registros mediante los métodos **Move**.

El valor de la propiedad **CacheStart** es el marcador del primer registro del objeto **Recordset** que se va a almacenar en la memoria caché. Puede usar el marcador de un registro para establecer la propiedad **CacheStart**. Convierta el registro que desee que comience la memoria caché en el registro actual y establezca la propiedad **CacheStart** con el mismo valor que la propiedad **[Bookmark](recordset-bookmark-property-dao.md)**.

El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché en la caché y solicita registros fuera del intervalo de caché en el servidor.

Los registros recuperados de la caché no reflejan los cambios realizados simultáneamente en el origen de datos por otros usuarios.

Para forzar una actualización de todos los datos almacenados en la memoria caché, establezca la propiedad **CacheSize** del objeto **Recordset** en 0, restablézcala al tamaño de la memoria caché que solicitó originalmente y, finalmente, use el método **FillCache**.

