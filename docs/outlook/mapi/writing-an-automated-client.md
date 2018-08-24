---
title: Escribir a un cliente automatizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 504e10efa4f540d64469f6aaab22b3f9e9e1157d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582556"
---
# <a name="writing-an-automated-client"></a>Escribir a un cliente automatizado

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Una aplicación cliente automatizada es una aplicación que se ejecute desatendida, no mostrar ninguna interfaz de usuario.
  
 De forma predeterminada, muchos de los métodos de interfaz MAPI mostrar una interfaz de usuario. Todos estos métodos tienen marcas que permite que un cliente permitir o suprimir esta presentación. Aunque MAPI espera que los proveedores de servicios de cumplimiento de estos marcadores, hay algunos proveedores que no siempre cumplen estas expectativas. Un motivo legítimo para no teniendo en cuenta los indicadores es la dependencia del proveedor de servicios de otro servicio que no permite la supresión de la interfaz de usuario. Si está desarrollando a un cliente automatizado, preste especial atención a los proveedores de servicios que se está usando y cómo están configurados. No asuma que todas las llamadas para suprimir una interfaz de usuario se completará correctamente. 
  
Clientes automatizados deben tener la información necesaria disponible para la configuración correcta de cada uno de los servicios de mensaje en el perfil. Hay dos formas de proporcionar información de configuración en tiempo de inicio de sesión:
  
- El proveedor de servicios puede recuperar información del perfil.
    
- El proveedor de servicios puede preguntar al usuario para obtener información. 
    
Puesto que la segunda opción es no disponible para los clientes automatizados, estos clientes deben usar la primera opción. Los clientes deben configurar sus perfiles con cuidado para asegurarse de que esta opción siempre funciona.
  
Los clientes automatizados siempre establecer la marca MAPI_NO_MAIL en la llamada a la función [MAPILogonEx](mapilogonex.md) para iniciar una sesión de MAPI. 
  

