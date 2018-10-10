---
title: GetChildren (método, ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a11f3e34f8dcb45bab88d8ff87e69067103e4640
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483854"
---
# <a name="getchildren-method-ado"></a>GetChildren (método, ADO)


**Se aplica a**: Access 2013 | Office 2013


Devuelve un objeto [Recordset](recordset-object-ado.md) cuyas filas representan los elementos secundarios de un objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxis

**Establecer** *conjunto de registros*  =  *registro*. GetChildren

## <a name="return-value"></a>Valor devuelto

Objeto **Recordset** cuyas filas representan los elementos secundarios del actual objeto **Record**. Por ejemplo, los elementos secundarios de un objeto **Record** que representa un directorio serían los archivos y subdirectorios incluidos en el directorio primario.

## <a name="remarks"></a>Comentarios

El proveedor determina qué columnas hay en el objeto **Recordset** devuelto. Por ejemplo, un proveedor de orígenes de documentos siempre devuelve un objeto **Recordset** de recurso.

