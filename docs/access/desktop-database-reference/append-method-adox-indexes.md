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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297098"
---
# <a name="append-method-adox-indexes"></a>Append (método, Indexes de ADOX)


**Se aplica a:** Access 2013, Office 2013



Agrega un nuevo objeto [Index](index-object-adox.md) a la colección [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Sintaxis

*Índices*. Anexar*Índice* \[,*columnas*\]

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Index* |El objeto **Index** que se anexará o el nombre del índice que se creará y anexará.|
|*Columns* |Opcional. Un valor **Variant** que especifica los nombres de las columnas que se van a indizar. El parámetro *Columns* corresponde a los valores de la propiedad [Name](name-property-adox.md) de los objetos [Column](column-object-adox.md).|

## <a name="remarks"></a>Comentarios

El parámetro *Columns* puede tomar el nombre de una columna, o bien, de una matriz de nombres de columna.

Si el proveedor no admite la creación de índices, se producirá un error.

