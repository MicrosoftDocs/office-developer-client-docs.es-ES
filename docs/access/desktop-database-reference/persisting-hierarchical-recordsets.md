---
title: Almacenar conjuntos de registros jerárquicos
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55f005818ef8fa44a2ee59542aa220f4d71eb687
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944987"
---
# <a name="persisting-hierarchical-recordsets"></a>Almacenar conjuntos de registros jerárquicos

**Se aplica a**: Access 2013, Office 2013

Puede guardar un objeto **Recordset** jerárquico en un archivo, en formato ADTG o XML, llamando al método [Save](save-method-ado.md). Sin embargo, se aplican dos limitaciones cuando se guardan objetos **Recordset** jerárquicos en formato XML: no se puede guardar en XML si el objeto **Recordset** jerárquico contiene actualizaciones pendientes y no se puede guardar un objeto **Recordset** jerárquico parametrizado.

Para obtener más información sobre el proveedor para forma de datos, vea [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) y el Servicio de forma de datos para OLE DB (OLE DB).

