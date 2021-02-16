---
title: Acción de macro ChangeView (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Puedes usar la acción ChangeView para navegar entre vistas en su lugar.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425361"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>Acción de macro ChangeView (aplicación web personalizada de Access)

Puedes usar la acción **ChangeView** para navegar entre vistas en su lugar. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La **acción ChangeView** tiene los siguientes argumentos. 
  
|**Argumento de la acción**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
|Tabla  <br/> |Sí  <br/> |Nombre de la tabla que se va a abrir.  <br/> |
|Ver  <br/> |Sí  <br/> |Nombre de la vista que se va a abrir.  <br/> |
|Donde  <br/> |No  <br/> |Si se especifica, reemplaza la condición WHERE del origen de registros del objeto.  <br/> |
|Ordenar por  <br/> |No  <br/> |Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales. De forma predeterminada, este argumento está en blanco.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cualquier ordenación o filtrado aplicado por el usuario se borra cuando se llama a la acción **ChangeView.** 
  
El  *argumento OrderBy*  es el nombre del campo o campos en los que desea ordenar los registros. Si usa más de un nombre de campo, separe los nombres con una coma (,). 
  
Cuando se establece el  *argumento OrderBy,*  los registros se ordenan de forma predeterminada en orden ascendente. 
  

