---
title: ParentRow (propiedad, ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950156"
---
# <a name="parentrow-property-ado"></a>ParentRow (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Establece el contenedor de un objeto **Row** de OLE DB en un objeto **ADORecordConstruction**, de modo que la página origen de la fila se convierta en un objeto **Record** de ADO.

Sólo escritura.

## <a name="syntax"></a>Sintaxis

Poner HRESULT\_ParentRow (\[en\] IUnknown\* pParent);

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*pParent* |Contenedor de una fila.|

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.

## <a name="applies-to"></a>Se aplica a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

