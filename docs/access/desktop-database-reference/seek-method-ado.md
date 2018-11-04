---
title: Seek (método) - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be8127ea3f298a8f137012615b1f4de656a6ea1f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949715"
---
# <a name="seek-method-ado"></a>Seek (método, ADO)

**Se aplica a**: Access 2013, Office 2013

Busca en el índice de un objeto [Recordset](recordset-object-ado.md) para localizar rápidamente la fila que coincida con los valores especificados, y cambia la posición de fila actual a dicha fila.

## <a name="syntax"></a>Sintaxis

*conjunto de registros*. Seek*KeyValues*, *SeekOption*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*KeyValues* |Matriz de valores **Variant**. Un índice consta de una o varias columnas y la matriz contiene un valor que se va a comparar con cada columna correspondiente.|
|*SeekOption* |Valor de [SeekEnum](seekenum.md) que especifica el tipo de comparación que se va a realizar entre las columnas del índice y el valor de *KeyValues* correspondiente.|

## <a name="remarks"></a>Comentarios

Use el método **Seek** junto con la propiedad [Index](index-property-ado.md) si el proveedor subyacente admite índices en el objeto **Recordset**. Use el método de **(adSeek)** [admite](supports-method-ado.md)para determinar si el proveedor subyacente admite **Seek**y el método **Supports** para determinar si el proveedor admite índices. Por ejemplo, el [proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) admite **Seek** e **Index**.

Si **Seek** no encuentra la fila deseada, no se produce ningún error y la fila se coloca al final del objeto **Recordset**. Establezca la propiedad **Index** en el índice deseado antes de ejecutar este método.

Este método se puede usar sólo con cursores de servidor. Seek no se admite cuando el valor de la propiedad **CursorLocation** del objeto [Recordset](cursorlocation-property-ado.md) es **adUseClient**.

Este método se puede usar únicamente cuando el objeto **Recordset** se ha abierto con un valor [adCmdTableDirect](commandtypeenum.md) de **CommandTypeEnum**.

