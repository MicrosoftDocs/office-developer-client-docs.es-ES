---
title: Chapter (propiedad, ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7523a930feed7431bf8be0bbb7222a4b305483
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949400"
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

