---
title: Recordset, SourceRecordset (propiedades, RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21176e050c77b0f14fcb03b054e8a1ab692df7d5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949260"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset, SourceRecordset (propiedades, RDS)

**Se aplica a**: Access 2013, Office 2013

Indica el objeto **Recordset** devuelto desde un objeto de negocio personalizado.

## <a name="syntax"></a>Sintaxis

*DataControl*. SourceRecordset = *conjunto de registros*

*Conjunto de registros* = *DataControl*. Conjunto de registros

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*Recordset* |Variable de objeto que representa un objeto **Recordset**.|

## <a name="remarks"></a>Comentarios

Es posible establecer la propiedad **SourceRecordset** en un objeto [Recordset](recordset-object-ado.md) devuelto desde un objeto de negocio personalizado.

Estas propiedades permiten que una aplicación controle el proceso de enlace por medio de un proceso personalizado. Reciben un conjunto de filas ajustado a un objeto **Recordset** para poder interactuar directamente con el objeto **Recordset**, realizar acciones como establecer propiedades o iterar a lo largo del objeto **Recordset**.

Es posible establecer la propiedad **SourceRecordset** o leer la propiedad **Recordset** en tiempo de ejecución en el código de scripting.

**SourceRecordset** es una propiedad de solo escritura, al contrario que la propiedad **Recordset**, que es de solo lectura.

