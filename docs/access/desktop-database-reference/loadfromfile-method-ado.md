---
title: LoadFromFile (método, ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9316bc4302a559fa44082a0576595707157e9d64
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708462"
---
# <a name="loadfromfile-method-ado"></a>LoadFromFile (método, ADO)

**Se aplica a**: Access 2013, Office 2013

Carga el contenido de un archivo existente en un objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Secuencia*. LoadFromFile *FileName*

## <a name="parameters"></a>Parámetros

|Nombre |Descripción|
|:----|:----------|
|*FileName* |Valor de tipo **String** que contiene el nombre del archivo que se va a cargar en el objeto **Stream**. *Nombre de archivo* puede contener cualquier ruta de acceso válida y un nombre en formato UNC. Si no existe el archivo especificado, se produce un error en tiempo de ejecución.|

## <a name="remarks"></a>Comentarios

Este método se puede utilizar para cargar el contenido de un archivo local en un objeto **Stream**; por ejemplo, para cargar el contenido de un archivo local en un servidor.

El objeto **Stream** ya debe estar abierto antes de que se llame a **LoadFromFile**. Este método no cambia el enlace del objeto **Stream**; seguirá enlazado al objeto especificado por la dirección URL o el objeto **Record** con el que se abrió originalmente el objeto **Stream**.

**LoadFromFile** sobrescribe el contenido actual del objeto **Stream** con los datos del archivo que se leen. Los bytes existentes en el objeto **Stream** se sobrescriben con el contenido del archivo. Se truncan los bytes que existían anteriormente o que permanecen después de [EOS](eos-property-ado.md) que crea **LoadFromFile**.

Tras llamar a **LoadFromFile**, la posición actual se establece en el principio del objeto **Stream** (el valor de [Position](position-property-ado.md) es 0).

Dado que se pueden agregar 2 bytes al principio de la secuencia para la codificación, puede que el tamaño de la secuencia no coincida exactamente con el tamaño del archivo desde el cual se cargó.

