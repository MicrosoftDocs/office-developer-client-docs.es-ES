---
title: Propiedad DataMember (ADO)
TOCTitle: DataMember property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 410f11af8daf3912dca9dc78a1cb9216ff8f8dd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294496"
---
# <a name="datamember-property-ado"></a>Propiedad DataMember (ADO)

**Se aplica a:** Access 2013, Office 2013

Indica el nombre del miembro de datos que se va a recuperar del objeto al que hace referencia la propiedad [DataSource](datasource-property-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String**. El nombre no distingue entre mayúsculas y minúsculas.

## <a name="remarks"></a>Comentarios

Esta propiedad se usa para crear controles enlazados a datos con el Entorno de datos. El Entorno de datos mantiene colecciones de datos (orígenes de datos) que contienen objetos con nombre (*miembros de datos*) que se representarán como un objeto [ Recordset](recordset-object-ado.md). 

Las propiedades **DataMember** y **DataSource** deben utilizarse conjuntamente.

La propiedad **DataMember** determina cuál de los objetos especificados por la propiedad **DataSource** se va a representar como un objeto **Recordset**. El objeto **Recordset** debe estar cerrado para que se pueda establecer esta propiedad. Se genera un error si no se establece la propiedad **DataMember** antes de establecerse la propiedad **DataSource**, o bien, si el objeto especificado en la propiedad **DataSource** no reconoce el nombre de **DataMember**.

**Uso**

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
