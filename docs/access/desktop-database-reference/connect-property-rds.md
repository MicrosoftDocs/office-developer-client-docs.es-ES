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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706740"
---
# <a name="connect-property-rds"></a>Connect (propiedad, RDS)

**Se aplica a**: Access 2013, Office 2013

Indica el nombre de la base de datos desde la que se ejecutan las operaciones de consulta y actualización.

La propiedad **Connect** se puede establecer en tiempo de diseño en las etiquetas OBJECT del objeto [RDS.DataControl](datacontrol-object-rds.md), o bien en tiempo de ejecución en el código del scripting (por ejemplo, VBScript).

## <a name="syntax"></a>Sintaxis

Tiempo de diseño: \<PARAM NAME = "Conectar" valor = "ConnectionString"\>

Tiempo de ejecución: DataControl.Connect = "ConnectionString"

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*ConnectionString* |Cadena de conexión válida. Para obtener información más general sobre las cadenas de conexión, vea la propiedad [ConnectionString](connectionstring-property-ado.md) o vea la documentación de su proveedor.<br/><br/>**Nota**: si especifica MS Remote como el proveedor para el **RDS. DataControl** crearía un escenario de cuatro niveles. No se han probado los escenarios de más de tres niveles y, en principio, no son necesarios.|
|*DataControl* |Variable de objeto que representa un objeto **RDS.DataControl**.|

