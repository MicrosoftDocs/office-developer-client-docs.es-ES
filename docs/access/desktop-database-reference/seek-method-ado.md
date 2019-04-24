---
title: 'Seek (método): ActiveX Data Objects (ADO)'
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308795"
---
# <a name="seek-method-ado"></a>Seek (método, ADO)

**Se aplica a:** Access 2013, Office 2013

Busca en el índice de un objeto [Recordset](recordset-object-ado.md) para localizar rápidamente la fila que coincida con los valores especificados, y cambia la posición de fila actual a dicha fila.

## <a name="syntax"></a>Sintaxis

*objeto Recordset*. Seek*keyValues*, *SeekOption*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*KeyValues* |Matriz de valores **Variant**. Un índice consta de una o varias columnas y la matriz contiene un valor que se va a comparar con cada columna correspondiente.|
|*SeekOption* |Valor de [SeekEnum](seekenum.md) que especifica el tipo de comparación que se va a realizar entre las columnas del índice y el valor de *KeyValues* correspondiente.|

## <a name="remarks"></a>Comentarios

Use el método **Seek** junto con la propiedad [Index](index-property-ado.md) si el proveedor subyacente admite índices en el objeto **Recordset**. Use el método [Supports](supports-method-ado.md)**(adSeek)** para determinar si el proveedor subyacente admite **Seek**, y el método **Supports(adIndex)** para determinar si el proveedor admite índices. Por ejemplo, el [proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) admite **Seek** e **Index**.

Si **Seek** no encuentra la fila deseada, no se produce ningún error y la fila se coloca al final del objeto **Recordset**. Establezca la propiedad **Index** en el índice deseado antes de ejecutar este método.

Este método se puede usar sólo con cursores de servidor. Seek no se admite cuando el valor de la propiedad **CursorLocation** del objeto [Recordset](cursorlocation-property-ado.md) es **adUseClient**.

Este método se puede usar únicamente cuando el objeto **Recordset** se ha abierto con un valor [adCmdTableDirect](commandtypeenum.md) de **CommandTypeEnum**.

