---
title: Connect (propiedad, RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295985"
---
# <a name="connect-property-rds"></a>Connect (propiedad, RDS)

**Se aplica a:** Access 2013, Office 2013

Indica el nombre de la base de datos desde la que se ejecutan las operaciones de consulta y actualización.

La propiedad **Connect** se puede establecer en tiempo de diseño en las etiquetas OBJECT del objeto [RDS.DataControl](datacontrol-object-rds.md), o bien en tiempo de ejecución en el código del scripting (por ejemplo, VBScript).

## <a name="syntax"></a>Sintaxis

Tiempo de diseño \<: param name = "Connect" Value = "ConnectionString"\>

Tiempo de ejecución: DataControl. Connect = "ConnectionString"

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*ConnectionString* |Cadena de conexión válida. Para obtener información más general sobre las cadenas de conexión, vea la propiedad [ConnectionString](connectionstring-property-ado.md) o vea la documentación de su proveedor.<br/><br/>**Nota**: especificar MS Remote como proveedor del **RDS. DataControl** crearía un escenario de cuatro niveles. No se han probado los escenarios de más de tres niveles y, en principio, no son necesarios.|
|*DataControl* |Variable de objeto que representa un objeto **RDS.DataControl**.|

