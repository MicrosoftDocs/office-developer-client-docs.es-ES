---
title: Propiedad Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296398"
---
# <a name="chapter-property-ado"></a>Propiedad Chapter (ADO)

**Se aplica a:** Access 2013, Office 2013
 
Obtiene o establece un objeto **Chapter** de OLE DB de/en un objeto **ADORecordsetConstruction**. Cuando se usa **put \_ Chapter** para establecer el **objeto Chapter,** se convierte un subconjunto de filas en un objeto **Recordset** de ADO. De este modo, se establece el capítulo actual del objeto **Rowset**. Lectura y escritura.

## <a name="syntax"></a>Sintaxis

HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);

HRESULT put \_ Chapter( \[ in long \] lChapter);

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*plChapter* |Puntero al controlador de un capítulo.|
|*LChapter* |Controlador de un capítulo.|

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores HRESULT estándar, incluidos S \_ OK y E \_ FAIL.

## <a name="applies-to"></a>Se aplica a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

