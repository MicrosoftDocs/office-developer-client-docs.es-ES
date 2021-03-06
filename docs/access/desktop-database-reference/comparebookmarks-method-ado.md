---
title: Método CompareBookmarks (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296097"
---
# <a name="comparebookmarks-method-ado"></a>Método CompareBookmarks (ADO)

**Se aplica a:** Access 2013, Office 2013

Compara dos marcadores y devuelve una indicación de sus valores relativos.

## <a name="syntax"></a>Sintaxis

*resultado*  =  *recordset*. CompareBookmarks(*Bookmark1*, *Bookmark2*)

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de [CompareEnum](compareenum.md) que indica la posición de fila relativa de dos registros representados por sus marcadores.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Bookmark1* |Marcador de la primera fila.|
|*Bookmark2* |Marcador de la segunda fila.|

## <a name="remarks"></a>Comentarios

Los marcadores deben aplicarse al mismo objeto [Recordset](recordset-object-ado.md), o bien, a un objeto **Recordset** y su [duplicado](clone-method-ado.md). No se pueden comparar de manera confiable los marcadores de diferentes objetos **Recordset**, aunque se crearon a partir del mismo origen o comando. Tampoco se pueden comparar los marcadores de un objeto **Recordset** cuyo proveedor subyacente no admite comparaciones.

Un marcador identifica de manera única una fila de un objeto **Recordset**. Use la propiedad [Bookmark](bookmark-property-ado.md) de la fila actual para obtener su marcador.

Dado que el tipo de datos de un marcador es específico del proveedor, ADO lo expone como Variant. Por ejemplo, SQL Server marcadores son de tipo DBTYPE \_ R8 (Double). ADO expondrá este tipo como Variant con un subtipo Double.

Cuando se comparan marcadores, ADO no intenta aplicar ningún tipo de conversión. Los valores se pasan simplemente al proveedor donde se lleva a cabo la comparación. Si los marcadores que se pasan al método **CompareBookmarks** están almacenados en variables de diferentes tipos, puede que se genere el error de inconsistencia de tipos "Argumentos incorrectos, fuera del intervalo permitido o en conflicto con otros".

Un marcador no válido o incorrectamente creado generará un error.

