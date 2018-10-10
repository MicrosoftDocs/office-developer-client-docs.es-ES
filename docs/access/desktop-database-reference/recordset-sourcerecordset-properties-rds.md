---
title: Propiedades Recordset, SourceRecordset (RDS)
TOCTitle: Recordset, SourceRecordset Properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a66e803738c16d291817eb80e7f680ff9c3c71e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484824"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Propiedades Recordset, SourceRecordset (RDS)


**Se aplica a**: Access 2013 | Office 2013

Indica el objeto **Recordset** devuelto desde un objeto de negocio personalizado.

## <a name="syntax"></a>Sintaxis

*DataControl*. SourceRecordset = *conjunto de registros*

*Conjunto de registros* = *DataControl*. Conjunto de registros

## <a name="parameters"></a>Parámetros

  - *DataControl*

  - Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *Recordset*

  - Variable de objeto que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Es posible establecer la propiedad **SourceRecordset** en un objeto [Recordset](recordset-object-ado.md) devuelto desde un objeto de negocio personalizado.

Estas propiedades permiten que una aplicación controle el proceso de enlace por medio de un proceso personalizado. Reciben un conjunto de filas ajustado a un objeto **Recordset** para poder interactuar directamente con el objeto **Recordset**, realizar acciones como establecer propiedades o iterar a lo largo del objeto **Recordset**.

Es posible establecer la propiedad **SourceRecordset** o leer la propiedad **Recordset** en tiempo de ejecución en el código de scripting.

**SourceRecordset** es una propiedad de solo escritura, al contrario que la propiedad **Recordset**, que es de solo lectura.

