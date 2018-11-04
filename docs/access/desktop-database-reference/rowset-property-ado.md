---
title: Rowset (propiedad, ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5979cb42e2ed4a979dc07016a4bb02b8097994
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949792"
---
# <a name="rowset-property-ado"></a>Rowset (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Obtiene o establece un objeto **Rowset** de OLE DB desde o en un objeto **ADORecordsetConstruction**. Cuando use put\_conjunto de filas, el conjunto de filas se convierte en un objeto **Recordset** de ADO.

Lectura y escritura.

## <a name="syntax"></a>Sintaxis

Get HRESULT\_conjunto de filas (\[out, retval\] IUnknown\* \* ppRowset);

Poner HRESULT\_conjunto de filas (\[en\] IUnknown\* pRowset);

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*ppRowset* |Puntero a un objeto **Rowset** de OLE DB.|
|*PRowset* |Un objeto **Rowset** de OLE DB.|

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.

## <a name="applies-to"></a>Se aplica a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

