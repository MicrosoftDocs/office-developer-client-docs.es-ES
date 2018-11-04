---
title: Append (método, Indexes de ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a02e74bbbc1b24939784a89965bf0757be0cfe
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949407"
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

## <a name="remarks"></a>Comentarios

El parámetro *Columns* puede tomar el nombre de una columna o una matriz de nombres de columna.

Si el proveedor no admite la creación de índices, se producirá un error.

