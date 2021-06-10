---
title: Propiedad RowPosition (ADO)
TOCTitle: RowPosition property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84d3ad7cc5b3d43b15ac1113f6fa00932678ebc3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306863"
---
# <a name="rowposition-property-ado"></a>Propiedad RowPosition (ADO)

**Se aplica a:** Access 2013, Office 2013

Obtiene o establece un objeto **RowPosition** de OLE DB desde o en un objeto **ADORecordsetConstruction**. Cuando se usa **put \_ RowPosition** para establecer el **objeto RowPosition,** el objeto **Recordset** resultante usa el **objeto RowPosition** para determinar la fila actual.

Lectura y escritura.

## <a name="syntax"></a>Sintaxis

HRESULT get \_ RowPosition( \[ out, retval \] IUnknown \* \* ppRowPos);

HRESULT put \_ RowPosition( \[ in \] IUnknown \* pRowPos);

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*ppRowPos* |Puntero a un objeto **RowPosition** de OLE DB.|
|*PRowPos* |Un objeto **RowPosition** de OLE DB.|

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores HRESULT estándar, incluidos S \_ OK y E \_ FAIL.

## <a name="remarks"></a>Comentarios

Cuando se establece esta propiedad, si el objeto **Rowset** del objeto **RowPosition** es diferente al objeto **Rowset** del objeto **Recordset**, el primero sobrescribe al segundo. El mismo comportamiento se aplica al **capítulo** actual de **RowPosition**.

## <a name="applies-to"></a>Se aplica a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

