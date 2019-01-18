---
title: Rowset (propiedad, ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706145"
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

