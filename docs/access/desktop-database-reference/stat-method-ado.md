---
title: 'Método Stat: ActiveX data objects (ADO)'
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308556"
---
# <a name="stat-method-ado"></a>Método Stat (ADO)

**Se aplica a:** Access 2013, Office 2013

Recupera información acerca de un objeto **Stream**.

## <a name="syntax"></a>Sintaxis

Secuencia *larga.* Stat(*StatStg*, *StatFlag*)

## <a name="return-value"></a>Valor devuelto

Valor largo que indica el estado de la operación.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*StatStg* |Estructura STATSTG que se rellenará con información sobre la secuencia. La implementación del método Stat que utiliza el objeto Stream de ADO no rellena todos los campos de la estructura.|
|*StatFlag* |Especifica que este método no devuelve algunos de los miembros de la estructura STATSTG, por lo que se ahorra una operación de asignación de memoria. Los valores se toman de la enumeración STATFLAG.<br/><br/>La enumeración STATFLAG tiene dos valores:<br/>- STATFLAG_DEFAULT: 0<br/>- STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Comentarios

La versión del método Stat implementada para el objeto Stream de ADO rellena los siguientes campos de la estructura STATSTG:

|Field|Descripción|
|:--------|:----------|
|*pwcsName* |Una cadena que contiene el nombre de la secuencia, si hay una disponible y no se especificó el valor StatFlag STATFLAG \_ NONAME.|
|*cbSize* |Especifica el tamaño en bytes de la matriz de secuencias o de bytes.|
|*mtime* |Indica la hora de la última modificación de esta matriz de bytes, secuencias o de almacenamiento.|
|*ctime* |Indica la hora de creación de esta matriz de bytes, secuencias o de almacenamiento.|
|*atime* |Indica la hora del último acceso a esta matriz de bytes, secuencias o de almacenamiento.|

Si se especifica STATFLAG NONAME en el parámetro StatFlag, no se devuelve el nombre de \_ la secuencia.

Si no se especificó STATFLAG NONAME en el parámetro StatFlag y no hay ningún nombre disponible para la secuencia actual, este valor \_ será E \_ NOTIMPL.

