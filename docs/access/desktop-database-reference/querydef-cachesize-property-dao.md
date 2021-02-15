---
title: Propiedad QueryDef.CacheSize (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301095"
---
# <a name="querydefcachesize-property-dao"></a>Propiedad QueryDef.CacheSize (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché. **Long** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . CacheSize

*expression* Variable que representa un objeto **QueryDef**.

## <a name="remarks"></a>Comentarios

El valor de la propiedad **CacheSize** debe estar entre 5 y 1200, pero no debe ser mayor que lo que permita la memoria disponible. Un valor típico es 100. El valor 0 desactiva el almacenamiento en caché.

El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché en la caché y solicita registros fuera del intervalo de caché en el servidor.

Los registros recuperados de la caché no reflejan los cambios simultáneos realizados por otros usuarios en el origen de datos.

