---
title: Configurar el formato de cálculo de secuencias de DCOM
TOCTitle: Setting DCOM Stream Marshaling Format
ms:assetid: 5f75fc59-a9f8-6686-07f9-de292e4da787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249346(v=office.15)
ms:contentKeyID: 48545162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51449286d2ddd9340f1adc883cdaff7e76429f88
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874114"
---
# <a name="setting-dcom-stream-marshaling-format"></a>Configurar el formato de cálculo de secuencias de DCOM


**Se aplica a**: Access 2013, Office 2013

Un equipo cliente que usa componentes de RDS 1.5 (o de una versión anterior) no es compatible con un servidor que usa componentes de RDS 2.0 (o de versiones posteriores). Cuando se usa DCOM como protocolo subyacente, RDS 2.0 (o versión posterior) resulta más eficiente para transportar objetos [Recordset](recordset-object-ado.md). Si el cliente ejecuta componentes de RDS 1.5 (o versiones anteriores), es posible configurar el servidor de modo que funcione con la compatibilidad RDS anterior (denominada RDS 1.0) o con la nueva compatibilidad RDS (denominada RDS 2.0 o posterior). Configure cualquiera de las siguientes entradas del Registro:

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS10" 
```

\-o -

```vb 
 
[HKEY_CLASSES_ROOT] 
\CLSID 
 \[58ECEE30-E715-11CF-B0E3-00AA003F000F} 
 \ADTGOptions]"MarshalFormat"="RDS20" 
```

