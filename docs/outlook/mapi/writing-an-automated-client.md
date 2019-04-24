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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325595"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="5d678-103">Escritura de un cliente automatizado</span><span class="sxs-lookup"><span data-stu-id="5d678-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="5d678-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d678-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d678-105">Una aplicación de cliente automatizada es una aplicación que se ejecuta en modo desatendido sin que se muestre ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d678-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="5d678-106">De forma predeterminada, muchos métodos de interfaz MAPI muestran una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d678-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="5d678-107">Todos estos métodos tienen marcas que permiten a un cliente permitir o suprimir esta presentación.</span><span class="sxs-lookup"><span data-stu-id="5d678-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="5d678-108">Aunque MAPI espera que los proveedores de servicios respeten estas marcas, hay algunos proveedores que no siempre cumplen estas expectativas.</span><span class="sxs-lookup"><span data-stu-id="5d678-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="5d678-109">Una razón legítima para no respetar los marcadores es la dependencia del proveedor de servicios en otro servicio que no permite la supresión de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5d678-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="5d678-110">Si está desarrollando un cliente automatizado, preste especial atención a los proveedores de servicios que utiliza y al modo en que se configuran.</span><span class="sxs-lookup"><span data-stu-id="5d678-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="5d678-111">No asuma que todas las llamadas para suprimir una interfaz de usuario se realizarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d678-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="5d678-112">Los clientes automatizados deben tener disponible la información necesaria para configurar correctamente cada uno de los servicios de mensajes en el perfil.</span><span class="sxs-lookup"><span data-stu-id="5d678-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="5d678-113">Hay dos formas de suministrar información de configuración en el momento del inicio de sesión:</span><span class="sxs-lookup"><span data-stu-id="5d678-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="5d678-114">El proveedor de servicios puede recuperar información del perfil.</span><span class="sxs-lookup"><span data-stu-id="5d678-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="5d678-115">El proveedor de servicios puede solicitar información al usuario.</span><span class="sxs-lookup"><span data-stu-id="5d678-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="5d678-116">Como la segunda opción no está disponible para los clientes automatizados, estos clientes deben usar la primera opción.</span><span class="sxs-lookup"><span data-stu-id="5d678-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="5d678-117">Los clientes deben configurar los perfiles con cuidado para asegurarse de que esta opción funciona siempre.</span><span class="sxs-lookup"><span data-stu-id="5d678-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="5d678-118">Los clientes automatizados siempre establecen la marca MAPI_NO_MAIL en la llamada de función [MAPILogonEx](mapilogonex.md) para iniciar una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="5d678-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

