---
title: Método Stat - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3853c42fab9de9e06691ae0e8efe20e23c410121
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949295"
---
# <a name="stat-method-ado"></a>Stat (método, ADO)

**Se aplica a**: Access 2013, Office 2013

Recupera información acerca de un objeto **Stream**.

## <a name="syntax"></a>Sintaxis

*Secuencia*de tipo Long. Stat (*StatStg*, *StatFlag*)

## <a name="return-value"></a>Valor devuelto

Valor largo que indica el estado de la operación.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*StatStg* |Estructura STATSTG que se rellenará con información sobre la secuencia. La implementación del método Stat que utiliza el objeto Stream de ADO no rellena todos los campos de la estructura.|
|*StatFlag* |Especifica que este método no devuelve algunos de los miembros de la estructura STATSTG, por lo que se ahorra una operación de asignación de memoria. Los valores se toman de la enumeración STATFLAG.<br/><br/>La enumeración STATFLAG tiene dos valores:<br/>-STATFLAG_DEFAULT: 0<br/>-STATFLAG_NONAME: 1 |


## <a name="remarks"></a>Comentarios

La versión del método Stat implementada para el objeto Stream de ADO rellena los siguientes campos de la estructura STATSTG:

|Campo|Descripción|
|:--------|:----------|
|*pwcsName* |El valor de una cadena que contiene el nombre de la secuencia, si está disponible y la StatFlag STATFLAG\_sin nombre no se ha especificado.|
|*cbSize* |Especifica el tamaño en bytes de la matriz de secuencias o de bytes.|
|*mtime* |Indica la hora de la última modificación de esta matriz de bytes, secuencias o de almacenamiento.|
|*ctime* |Indica la hora de creación de esta matriz de bytes, secuencias o de almacenamiento.|
|*atime* |Indica la hora del último acceso a esta matriz de bytes, secuencias o de almacenamiento.|

Si STATFLAG\_sin nombre se especifica en el parámetro StatFlag, el nombre de la secuencia no se devuelve.

Si STATFLAG\_sin nombre no se ha especificado en el parámetro StatFlag y no hay ningún nombre disponible para la secuencia actual, este valor será E\_NOTIMPL.

