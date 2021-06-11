---
title: Acción de macro RequeryRecords (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Puede usar la acción RequeryRecords para actualizar, ordenar y filtrar los datos de la vista activa consultando de nuevo el origen de la vista.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439250"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>Acción de macro RequeryRecords (aplicación web personalizada de Access)

Puede usar la acción **RequeryRecords** para actualizar, ordenar y filtrar los datos de la vista activa consultando de nuevo el origen de la vista. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La **acción RequeryRecords** tiene los argumentos siguientes. 
  
|**Parámetro**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
|**Where=** <br/> |No  <br/> |Una SQL where que restringe los registros de la vista. De forma predeterminada, este argumento está en blanco.  <br/> |
|**OrderBy** <br/> |No  <br/> |Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales. De forma predeterminada, este argumento está en blanco.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cualquier ordenación o filtrado aplicado por el usuario se borra cuando se llama a la acción **RequeryRecords.** 
  
El  *argumento OrderBy*  es el nombre del campo o campos en los que desea ordenar los registros. Si usa más de un nombre de campo, separe los nombres con una coma (,). 
  
Al establecer el argumento  *OrderBy,*  los registros se ordenan de forma predeterminada en orden ascendente. 
  
Para ordenar los registros en orden descendente, escriba DESC al final de la expresión de argumento *OrderBy.* Por ejemplo, para ordenar los registros de clientes en orden descendente por nombre de contacto, establezca el argumento  *OrderBy*  en "ContactName DESC". 
  
Para ordenar los nombres por LastName descendente y FirstName ascendente, establezca el argumento  *OrderBy*  en "LastName DESC, FirstName ASC". 
  

