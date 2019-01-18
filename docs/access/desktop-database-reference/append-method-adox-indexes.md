---
title: Append (método, Indexes de ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707559"
---
# <a name="append-method-adox-indexes"></a>Append (método, Indexes de ADOX)


**Se aplica a**: Access 2013, Office 2013



Agrega un nuevo objeto [Index](index-object-adox.md) a la colección [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Los índices*. Anexe el*índice* \[,*columnas*\]

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Index* |El objeto **Index** que se anexará o el nombre del índice que se creará y anexará.|
|*Columns* |Opcional. Un valor **Variant** que especifica los nombres de las columnas que se van a indizar. El parámetro *Columns* corresponde a los valores de la propiedad [Name](name-property-adox.md) de un objeto [Column](column-object-adox.md) u objetos.|

## <a name="remarks"></a>Observaciones

El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.

Si el proveedor no admite la creación de índices, se producirá un error.

