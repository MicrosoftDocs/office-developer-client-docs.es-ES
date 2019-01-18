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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701712"
---
# <a name="querydefcachesize-property-dao"></a>Propiedad QueryDef.CacheSize (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve el número de registros recuperados de un origen de datos ODBC que se almacenarán localmente en caché. **Long** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . CacheSize

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

El valor de la propiedad **CacheSize** debe estar entre 5 y 1200, pero no debe ser mayor que lo que permita la memoria disponible. Un valor típico es 100. El valor 0 desactiva el almacenamiento en caché.

El motor de base de datos de Microsoft Access solicita registros dentro del intervalo de caché en la caché y solicita registros fuera del intervalo de caché en el servidor.

Los registros recuperados de la caché no reflejan los cambios simultáneos realizados por otros usuarios en el origen de datos.

