---
title: RowPosition (propiedad, ADO)
TOCTitle: RowPosition Property (ADO)
ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15)
ms:contentKeyID: 48547325
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a4512157e70f4f5a7533e2a480dd96aa3693741
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484209"
---
# <a name="rowposition-property-ado"></a>RowPosition (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013



Obtiene o establece un objeto **RowPosition** de OLE DB desde o en un objeto **ADORecordsetConstruction**. Al usar **colocar\_RowPosition** para establecer el objeto **RowPosition** , el objeto **Recordset** resultante utiliza el objeto **RowPosition** para determinar la fila actual.

Lectura y escritura.

## <a name="syntax"></a>Sintaxis

Get HRESULT\_RowPosition (\[out, retval\] IUnknown\* \* ppRowPos);

Poner HRESULT\_RowPosition (\[en\] IUnknown\* pRowPos);

## <a name="parameters"></a>Parámetros

  - *ppRowPos*

  - Puntero a un objeto **RowPosition** de OLE DB.

  - *PRowPos*

  - Un objeto **RowPosition** de OLE DB.

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.

## <a name="remarks"></a>Comentarios

Cuando se establece esta propiedad, si el objeto **Rowset** del objeto **RowPosition** es diferente al objeto **Rowset** del objeto **Recordset**, el primero sobrescribe al segundo. El mismo comportamiento se aplica al **capítulo** actual de **RowPosition**.

## <a name="applies-to"></a>Se aplica a

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

