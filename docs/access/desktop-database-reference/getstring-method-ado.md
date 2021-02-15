---
title: Método GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292191"
---
# <a name="getstring-method-ado"></a>Método GetString (ADO)

**Se aplica a:** Access 2013, Office 2013

Devuelve el objeto [Recordset](recordset-object-ado.md) en forma de cadena.

## <a name="syntax"></a>Sintaxis

*Variant*  =  *recordset*. GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)

## <a name="return-value"></a>Valor devuelto

Devuelve el objeto **Recordset** como **Variant** de valores de cadena (BSTR).

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*StringFormat* |Valor de [StringFormatEnum](stringformatenum.md) que especifica cómo debe convertirse el objeto **Recordset** en una cadena. Los parámetros *RowDelimiter*, *ColumnDelimiter* y *NullExpr* se utilizan sólo cuando el valor de *StringFormat* es **adClipString**.|
|*NumRows* |Es opcional. Número de filas del objeto **Recordset** que se van a convertir. Si no se especifica *NumRows* o si es mayor que el número total de filas en el objeto **Recordset**, se convertirán todas las filas del objeto **Recordset**.|
|*ColumnDelimiter* |Es opcional. Delimitador que se utiliza entre las columnas, si se ha especificado; en caso contrario, el carácter de tabulación.|
|*RowDelimiter* |Es opcional. Delimitador que se utiliza entre las filas, si se ha especificado; en caso contrario, el carácter de retorno de carro.|
|*NullExpr* |Es opcional. Expresión que se utiliza en lugar de un valor nulo, si se ha especificado; en caso contrario, la cadena vacía.|

## <a name="remarks"></a>Comentarios

En la cadena se guardan los datos de fila y no los datos de esquema. Por lo tanto, no se puede volver a abrir un objeto **Recordset** mediante esta cadena.

Este método es equivalente al método **GetClipString** de RDO.

