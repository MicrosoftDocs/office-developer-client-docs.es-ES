---
title: Persistencia de los conjuntos de registros jerárquicos
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287583"
---
# <a name="persisting-hierarchical-recordsets"></a>Persistencia de los conjuntos de registros jerárquicos

**Se aplica a:** Access 2013, Office 2013

Puede guardar un objeto **Recordset** jerárquico en un archivo, en formato ADTG o XML, llamando al método [Save](save-method-ado.md). Sin embargo, se aplican dos limitaciones cuando se guardan objetos **Recordset** jerárquicos en formato XML: no se puede guardar en XML si el objeto **Recordset** jerárquico contiene actualizaciones pendientes y no se puede guardar un objeto **Recordset** jerárquico parametrizado.

Para obtener más información sobre el proveedor para forma de datos, vea [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) y el Servicio de forma de datos para OLE DB (OLE DB).

