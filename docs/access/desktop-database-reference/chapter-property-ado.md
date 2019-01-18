---
title: Chapter (propiedad, ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717940"
---
# <a name="chapter-property-ado"></a>Chapter (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013
 
Obtiene o establece un objeto **Chapter** de OLE DB de/en un objeto **ADORecordsetConstruction**. Al usar **colocar\_capítulo** para establecer el objeto **Chapter** , un subconjunto de filas se convierte en un objeto **Recordset** de ADO. De este modo, se establece el capítulo actual del objeto **Rowset**. Lectura/Escritura.

## <a name="syntax"></a>Sintaxis

Get HRESULT\_capítulo (\[out, retval\] largo\* plChapter);

Poner HRESULT\_capítulo (\[en\] lChapter largo);

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*plChapter* |Puntero al controlador de un capítulo.|
|*LChapter* |Controlador de un capítulo.|

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.

## <a name="applies-to"></a>Se aplica a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

