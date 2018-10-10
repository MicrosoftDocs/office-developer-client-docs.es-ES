---
title: Open (método, ADO MD)
TOCTitle: Open Method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad4d1c05637f2ff7ef5ff65ec26ab1b721495067
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483328"
---
# <a name="open-method-ado-md"></a>Open (método, ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Recupera los resultados de una consulta multidimensional y devuelve los resultados a un conjunto de celdas.

## <a name="syntax"></a>Sintaxis

*Conjunto de celdas*. Abrir*origen*, *ActiveConnection*

## <a name="parameters"></a>Parámetros

  - *Source*

  - Opcional. Un valor **Variant** que da como resultado una consulta multidimensional válida, como una consulta de expresión multidimensional (MDX). El argumento *Source* corresponde a la propiedad [Source](source-property-ado-md.md) . Para obtener más información acerca de MDX, vea la documentación de OLE DB para OLAP en el SDK de Microsoft Data Access Components.

  - *ActiveConnection*

  - Opcional. Un valor **Variant** que da como resultado una cadena que especifica un nombre válido de variable de objeto [Connection](connection-object-ado.md) de ADO o una definición para una conexión. El argumento *ActiveConnection* especifica la conexión en la que se va a abrir el objeto de [conjunto de celdas](cellset-object-ado-md.md) . Si pasa una definición de conexión para este argumento, ADO abre una conexión nueva con los parámetros especificados. El argumento *ActiveConnection* corresponde a la propiedad [ActiveConnection](activeconnection-property-ado-md.md) .

## <a name="remarks"></a>Comentarios

El método **Open** genera un error si se omite cualquiera de sus parámetros y si no se ha establecido el correspondiente valor de la propiedad antes de intentar abrir el **conjunto de celdas**.

