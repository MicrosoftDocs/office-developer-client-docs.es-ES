---
title: Refresh (método, RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e740d04b27b0154cd3621d870590cb522c2a239e
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026438"
---
# <a name="refresh-method-rds"></a>Refresh (método, RDS)

**Se aplica a**: Access 2013, Office 2013

Vuelve a consultar el origen de datos especificado en la propiedad [Connect](connect-property-rds.md) y actualiza los resultados de consulta.

## <a name="syntax"></a>Sintaxis

*DataControl*. Actualización

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Comentarios

Debe establecer las propiedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) y [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) antes de utilizar el método **Refresh**. Todos los controles enlazados a datos del formulario asociado a un objeto **RDS.DataControl** reflejarán el conjunto de registros nuevo. Se liberan todos los objetos [Recordset](recordset-object-ado.md) previamente existentes y se descartan todos los cambios no guardados. El método **Refresh** convierte automáticamente el primer registro en el registro actual.

Se recomienda llamar periódicamente al método **Refresh** cuando trabaja con datos. Si recupera datos y los deja durante un tiempo en el equipo de cliente, es probable que se vuelvan obsoletos. Es posible que se genere un error al realizar cambios porque otro usuario puede haber cambiado anteriormente el registro y enviado cambios.

