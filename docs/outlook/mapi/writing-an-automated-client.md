---
title: Escritura de un cliente automatizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439768"
---
# <a name="writing-an-automated-client"></a>Escritura de un cliente automatizado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una aplicación de cliente automatizada es una aplicación que se ejecuta en modo desatendido sin que se muestre ninguna interfaz de usuario.
  
 De forma predeterminada, muchos métodos de interfaz MAPI muestran una interfaz de usuario. Todos estos métodos tienen marcas que permiten a un cliente permitir o suprimir esta presentación. Aunque MAPI espera que los proveedores de servicios respeten estas marcas, hay algunos proveedores que no siempre cumplen estas expectativas. Una razón legítima para no respetar los marcadores es la dependencia del proveedor de servicios en otro servicio que no permite la supresión de la interfaz de usuario. Si está desarrollando un cliente automatizado, preste especial atención a los proveedores de servicios que utiliza y al modo en que se configuran. No asuma que todas las llamadas para suprimir una interfaz de usuario se realizarán correctamente. 
  
Los clientes automatizados deben tener disponible la información necesaria para configurar correctamente cada uno de los servicios de mensajes en el perfil. Hay dos formas de suministrar información de configuración en el momento del inicio de sesión:
  
- El proveedor de servicios puede recuperar información del perfil.
    
- El proveedor de servicios puede solicitar información al usuario. 
    
Como la segunda opción no está disponible para los clientes automatizados, estos clientes deben usar la primera opción. Los clientes deben configurar los perfiles con cuidado para asegurarse de que esta opción funciona siempre.
  
Los clientes automatizados siempre establecen la marca MAPI_NO_MAIL en la llamada de función [MAPILogonEx](mapilogonex.md) para iniciar una sesión MAPI. 
  

