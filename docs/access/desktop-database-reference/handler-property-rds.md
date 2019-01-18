---
title: Handler (propiedad, RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716008"
---
# <a name="handler-property-rds"></a>Handler (propiedad, RDS)

**Se aplica a**: Access 2013, Office 2013

Indica el nombre de un programa de personalización del servidor (controlador) que amplía la funcionalidad de [RDSServer.DataFactory](datafactory-object-rdsserver.md) y de cualquier parámetro utilizado por el *controlador*.

## <a name="syntax"></a>Sintaxis

*DataControl*. Controlador = *cadena*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Un valor de **tipo String** que contiene el nombre del controlador y de cualquier parámetro, todo separado por comas (por ejemplo, "handlerName, parm1, parm2,..., parm *N"*).|

## <a name="remarks"></a>Comentarios

Esta propiedad admite personalización, una funcionalidad que exige el establecimiento de la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient**.

El nombre del controlador y sus parámetros, si los hubiera, se separan mediante comas (","). La aparición de un punto y coma (";") en algún lugar de *String* dará lugar a un comportamiento impredecible. Puede escribir su propio controlador siempre que admita la interfaz **IDataFactoryHandler**.

El nombre del controlador predeterminado es **MSDFMAP.Handler**, mientras que su parámetro predeterminado es un archivo de personalización denominado **MSDFMAP.INI**. Utilice esta propiedad para llamar a archivos de personalización alternativos creados por el administrador del servidor.

La alternativa a establecer la propiedad **Handler** es especificar un controlador y parámetros en la propiedad [ConnectionString](connectionstring-property-ado.md) ; es decir, "**controlador = *** handlerName, parm1, parm2,...;*".

