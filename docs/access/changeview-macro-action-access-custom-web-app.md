---
title: Acción de Macro ChangeView (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Puede usar la acción ChangeView para navegar entre vistas en su lugar.
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815339"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>Acción de Macro ChangeView (aplicación web personalizado de Access)

Puede usar la acción **ChangeView** para navegar entre vistas en su lugar. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **ChangeView** tiene los siguientes argumentos. 
  
|**Argumento de la acción**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
|Tabla  <br/> |Sí  <br/> |El nombre de la tabla que se va a abrir.  <br/> |
|Vista  <br/> |Sí  <br/> |El nombre de la vista que se va a abrir.  <br/> |
|Donde  <br/> |No  <br/> |Si se especifica, reemplaza la condición WHERE del origen de registros del objeto.  <br/> |
|Order By  <br/> |No  <br/> |Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales. De forma predeterminada, este argumento está en blanco.  <br/> |
   
## <a name="remarks"></a>Notas

Ordenación o los filtros aplicados por el usuario está desactivada cuando se llama a la acción **ChangeView** . 
  
El argumento *OrderBy* es el nombre del campo o campos en el que desea ordenar los registros. Cuando utilice más de un nombre de campo, separe los nombres con una coma (,). 
  
Cuando se establece el argumento *OrderBy* , los registros se ordenan en orden ascendente de forma predeterminada. 
  

