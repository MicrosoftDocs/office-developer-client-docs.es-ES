---
title: Refresh (método, RDS)
TOCTitle: Refresh Method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9d7d1ecb009f61933328695ccbfbea06ac9d7b0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483904"
---
# <a name="refresh-method-rds"></a>Refresh (método, RDS)


**Se aplica a**: Access 2013 | Office 2013

Vuelve a consultar el origen de datos especificado en la propiedad [Connect](connect-property-rds.md) y actualiza los resultados de consulta.

## <a name="syntax"></a>Sintaxis

*DataControl*. Actualización

## <a name="parameters"></a>Parámetros

  - *DataControl*

  - Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).

## <a name="remarks"></a>Comentarios

Debe establecer las propiedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) y [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) antes de utilizar el método **Refresh**. Todos los controles enlazados a datos del formulario asociado a un objeto **RDS.DataControl** reflejarán el conjunto de registros nuevo. Se liberan todos los objetos [Recordset](recordset-object-ado.md) previamente existentes y se descartan todos los cambios no guardados. El método **Refresh** convierte automáticamente el primer registro en el registro actual.

Se recomienda llamar periódicamente al método **Refresh** cuando trabaja con datos. Si recupera datos y los deja durante un tiempo en el equipo de cliente, es probable que se vuelvan obsoletos. Es posible que se genere un error al realizar cambios porque otro usuario puede haber cambiado anteriormente el registro y enviado cambios.

