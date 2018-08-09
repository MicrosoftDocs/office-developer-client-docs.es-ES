---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Inicie sesión en el sitio de red social mediante la autenticación basada en formularios.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821126"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="18cb6-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="18cb6-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="18cb6-104">Inicie sesión en el sitio de red social mediante la autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="18cb6-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="18cb6-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18cb6-105">Parameters</span></span>

<span data-ttu-id="18cb6-106">_Configuración_</span><span class="sxs-lookup"><span data-stu-id="18cb6-106">_connectIn_</span></span>
  
> <span data-ttu-id="18cb6-107">[entrada] Una cadena que es **null**, una dirección URL a un formulario de inicio de sesión en el web o una cadena que contiene las credenciales de inicio de sesión, según el contexto en el proceso de inicio de sesión cuando se llama a este método.</span><span class="sxs-lookup"><span data-stu-id="18cb6-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="18cb6-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="18cb6-108">_connectOut_</span></span>
  
> <span data-ttu-id="18cb6-109">[out] Una cadena que contiene las credenciales de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="18cb6-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18cb6-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18cb6-110">Remarks</span></span>

<span data-ttu-id="18cb6-111">Outlook Social Connector (OSC) llama al método de **LogonWeb** sólo si el proveedor indica que admite la autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="18cb6-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="18cb6-112">El proveedor indica que requiere la autenticación basada en formularios mediante la configuración de **useLogonWebAuth** como **true** en el XML de **las capacidades**.</span><span class="sxs-lookup"><span data-stu-id="18cb6-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="18cb6-113">Si el proveedor establece **useLogonWebAuth** como **false**, el OSC usa la autenticación básica y llama al método [ISocialSession::Logon](isocialsession-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="18cb6-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="18cb6-114">Inicie sesión en un sitio de red social mediante la autenticación basada en formularios implica llamar a los métodos **LogonWeb** y [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) en un orden específico:</span><span class="sxs-lookup"><span data-stu-id="18cb6-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="18cb6-115">El OSC llama **LogonWeb** la primera vez, pasando **null** para el parámetro de _configuración_ .</span><span class="sxs-lookup"><span data-stu-id="18cb6-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="18cb6-116">El proveedor genera el error OSC_E_AUTH_ERROR para el OSC.</span><span class="sxs-lookup"><span data-stu-id="18cb6-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="18cb6-117">A continuación, el OSC llama a **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="18cb6-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="18cb6-118">El proveedor devuelve la dirección URL apropiada a una página de inicio de sesión en el método **GetLogonUrl** .</span><span class="sxs-lookup"><span data-stu-id="18cb6-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="18cb6-119">El OSC usa la dirección URL devuelta por **GetLogonUrl** para mostrar la página de inicio de sesión basado en formularios.</span><span class="sxs-lookup"><span data-stu-id="18cb6-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="18cb6-120">El OSC, a continuación, llama a **LogonWeb** una segunda vez, pasando la dirección URL para el formulario de inicio de sesión en el parámetro de _configuración_ .</span><span class="sxs-lookup"><span data-stu-id="18cb6-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="18cb6-121">Si la autenticación se realiza correctamente, el proveedor devuelve las credenciales de inicio de sesión en el parámetro _connectOut_ para el OSC.</span><span class="sxs-lookup"><span data-stu-id="18cb6-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="18cb6-122">Si se produce un error en la autenticación, el proveedor genera el error OSC_E_AUTH_ERROR para el OSC.</span><span class="sxs-lookup"><span data-stu-id="18cb6-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="18cb6-123">Si el proveedor OSC admite el inicio de sesión con credenciales almacenadas en caché, especifica **useLogonCached** como **true** en el XML de las **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="18cb6-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="18cb6-124">El proveedor debe colocar todas las credenciales de inicio de sesión en la cadena de _connectOut_ que el proveedor desea el OSC para almacenar a través de conexiones.</span><span class="sxs-lookup"><span data-stu-id="18cb6-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="18cb6-125">El OSC no interpreta la cadena _connectOut_ .</span><span class="sxs-lookup"><span data-stu-id="18cb6-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="18cb6-126">Una vez que el OSC comprueba que **useLogonCached** es **true**, el OSC cifra la cadena para la seguridad antes de almacenarlos en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="18cb6-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="18cb6-127">El OSC pasa esta cadena para el parámetro de _configuración_ en los intentos posteriores para iniciar sesión en la red social mediante una llamada a [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="18cb6-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="18cb6-128">Para obtener información sobre códigos de error, vea [Códigos de error del proveedor Outlook Social Connector](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="18cb6-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18cb6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="18cb6-129">See also</span></span>

- [<span data-ttu-id="18cb6-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18cb6-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="18cb6-131">Autenticación basada en formularios</span><span class="sxs-lookup"><span data-stu-id="18cb6-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

