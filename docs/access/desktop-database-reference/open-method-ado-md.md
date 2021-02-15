---
title: Open (método, ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288402"
---
# <a name="open-method-ado-md"></a>Open (método, ADO MD)

**Se aplica a:** Access 2013, Office 2013

Recupera los resultados de una consulta multidimensional y devuelve los resultados a un conjunto de celdas.

## <a name="syntax"></a>Sintaxis

*Conjunto de celdas*. Open *Source*, *ActiveConnection*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |Opcional. Un valor **Variant** que da como resultado una consulta multidimensional válida, como una consulta de expresión multidimensional (MDX). El argumento *Source* corresponde a la propiedad [Source](source-property-ado-md.md). Para obtener más información acerca de MDX, vea la documentación de OLE DB para OLAP en el SDK de Microsoft Data Access Components.|
|*ActiveConnection* |Opcional. Un valor **Variant** que da como resultado una cadena que especifica un nombre válido de variable de objeto [Connection](connection-object-ado.md) de ADO o una definición para una conexión. El argumento *ActiveConnection* especifica la conexión durante la que se abrirá el objeto [Cellset](cellset-object-ado-md.md). Si pasa una definición de conexión para este argumento, ADO abre una conexión nueva que utiliza los parámetros especificados. El argumento *ActiveConnection* corresponde a la propiedad [ActiveConnection](activeconnection-property-ado-md.md).|

## <a name="remarks"></a>Comentarios

El método **Open** genera un error si se omite cualquiera de sus parámetros y si no se ha establecido el correspondiente valor de la propiedad antes de intentar abrir el **conjunto de celdas**.

