---
title: Row (propiedad)-ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306485"
---
# <a name="row-property-ado"></a>Row (propiedad, ADO)

**Se aplica a:** Access 2013, Office 2013

Obtiene o establece un objeto **Row** de OLE DB desde o en un objeto **ADORecordConstruction**. Cuando se usa **Put\_Row** para establecer un objeto **Row** , una fila se convierte en un objeto **Record** de ADO. Lectura y escritura.

## <a name="syntax"></a>Sintaxis

HRESULT obtener\_fila (\[out, retval\] IUnknown\* \* ppRow);

HRESULT Put\_Row (\[en\] IUnknown\* pRow);

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*ppRow* |Puntero a un objeto **Row** de OLE DB.|
|*PRow* |Un objeto **Row** de OLE DB.|

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores HRESULT estándar, incluidos\_los errores S\_OK y e.

## <a name="applies-to"></a>Se aplica a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

