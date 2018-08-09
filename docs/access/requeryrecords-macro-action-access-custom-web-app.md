---
title: Acción de Macro RequeryRecords (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Puede usar la acción RequeryRecords para actualizar, ordenar y filtrar los datos en la vista activa por volver a consultar el origen de la vista.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815478"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>Acción de Macro RequeryRecords (aplicación web personalizado de Access)

Puede usar la acción **RequeryRecords** para actualizar, ordenar y filtrar los datos en la vista activa por volver a consultar el origen de la vista. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **RequeryRecords** tiene los siguientes argumentos. 
  
|**Parámetro**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
|**Donde =** <br/> |No  <br/> |Una cláusula WHERE de SQL que restringe los registros en la vista. De forma predeterminada, este argumento está en blanco.  <br/> |
|**OrderBy** <br/> |No  <br/> |Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales. De forma predeterminada, este argumento está en blanco.  <br/> |
   
## <a name="remarks"></a>Comentarios

Ordenación o los filtros aplicados por el usuario está desactivada cuando se llama a la acción **RequeryRecords** . 
  
El argumento *OrderBy* es el nombre del campo o campos en el que desea ordenar los registros. Cuando utilice más de un nombre de campo, separe los nombres con una coma (,). 
  
Cuando se establece el argumento *OrderBy* , los registros se ordenan en orden ascendente de forma predeterminada. 
  
Para ordenar los registros en orden descendente, escriba DESC al final de la expresión de argumento *OrderBy* . Por ejemplo, para ordenar los registros de clientes en orden descendente por nombre de contacto, establezca el argumento *OrderBy* en "ContactName DESC". 
  
Para ordenar los nombres de forma descendente, nombre y apellido ascendente, establezca el argumento *OrderBy* en "LastName DESC, FirstName ASC". 
  

