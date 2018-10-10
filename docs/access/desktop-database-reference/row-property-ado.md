---
title: Fila (propiedad) - ActiveX Data Objects (ADO)
TOCTitle: Row Property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05d97bb411c4199677f512d9412653ca5a4b4fe1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484760"
---
# <a name="row-property-ado"></a>Row (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013



Obtiene o establece un objeto **Row** de OLE DB desde o en un objeto **ADORecordConstruction**. Al usar **colocar\_fila** para establecer un objeto **Row** , una fila se convierta en un objeto **Record** de ADO. Lectura y escritura.

## <a name="syntax"></a>Sintaxis

Get HRESULT\_fila (\[out, retval\] IUnknown\* \* ppRow);

Poner HRESULT\_fila (\[en\] IUnknown\* pRow);

## <a name="parameters"></a>Parámetros

  - *ppRow*

  - Puntero a un objeto **Row** de OLE DB.

  - *PRow*

  - Un objeto **Row** de OLE DB.

## <a name="return-values"></a>Valores devueltos

Este método de propiedad devuelve los valores estándar HRESULT, incluidos S\_Aceptar y E\_producirá un error.

## <a name="applies-to"></a>Se aplica a

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

