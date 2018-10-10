---
title: Chapter (propiedad, ADO)
TOCTitle: Chapter Property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f02b20aef2b76ff00ce23b8597132dc22b414993
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485904"
---
# <a name="chapter-property-ado"></a>Chapter (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013
 

Obtiene o establece un objeto **Chapter** de OLE DB de/en un objeto **ADORecordsetConstruction**. Al usar **colocar\_capítulo** para establecer el objeto **Chapter** , un subconjunto de filas se convierte en un objeto **Recordset** de ADO. De este modo, se establece el capítulo actual del objeto **Rowset**. Lectura/Escritura.

## <a name="syntax"></a>Sintaxis

Get HRESULT\_capítulo (\[out, retval\] largo\* plChapter);

Poner HRESULT\_capítulo (\[en\] lChapter largo);

## <a name="parameters"></a>Parámetros

  - *plChapter*

  - Puntero al controlador de un capítulo.

  - *LChapter*

  - Controlador de un capítulo.

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.

## <a name="applies-to"></a>Se aplica a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

