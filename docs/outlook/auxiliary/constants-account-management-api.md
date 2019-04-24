---
title: Constantes (API de administración de cuenta)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2a15e5df-b8e3-9c37-b1ee-2881d010e30b
description: Este tema contiene definiciones de constantes, identificadores de clase e identificadores de interfaz para la API de administración de cuentas.
ms.openlocfilehash: 52d6e1801ac35621179aa0cac8acc2893aeb06b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316873"
---
# <a name="constants-account-management-api"></a>Constantes (API de administración de cuenta)

Este tema contiene definiciones de constantes, identificadores de clase e identificadores de interfaz para la API de administración de cuentas.
  
## <a name="constants"></a>Constantes

|**Constante**|**Definición**|
|:-----|:-----|
|ACCT_INIT_NOSYNCH_MAPI_ACCTS  <br/> |0x00000001  <br/> |
|ACCT_INIT_NO_STORES_CHECK  <br/> |0x00000002  <br/> |
|ACCTUI_NO_WARNING  <br/> |0x0100  <br/> |
|ACCTUI_SHOW_ACCTWIZARD  <br/> |0x0400  <br/> |
|ACCTUI_SHOW_DATA_TAB  <br/> |0x0200  <br/> |
|E_ACCT_NOT_FOUND  <br/> |0x800C8101  <br/> |
|E_ACCT_UI_BUSY  <br/> |0x800C8102  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |0x800C8105  <br/> |
|E_INVALIDARG  <br/> | *Tal y como se define en el archivo de encabezado Winerror. h del kit de desarrollo de software (SDK) de Windows.*  <br/> |
|E_NOTIMPL  <br/> | *Como se define en el archivo de encabezado Winerror. h de Windows SDK.*  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |0x800C8002  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |0x800C8005  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |0x800C8003  <br/> |
|E_OLK_PROP_READ_ONLY  <br/> |0x800C800D  <br/> |
|E_OLK_REGISTRY  <br/> |0x800C8001  <br/> |
|Las siguientes constantes que comienzan con ENCRYPT_ se usan en la propiedad [PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) para especificar el tipo de conexión cifrada.  <br/> ||
|ENCRYPT_CONN_AUTO  <br/> |3  <br/> |
|ENCRYPT_CONN_NO_SECURITY  <br/> |comprendi  <br/> |
|ENCRYPT_CONN_SSL  <br/> |1  <br/> |
|ENCRYPT_CONN_TLS  <br/> |segundo  <br/> |
|MAPIACCT_SEND_ONLY  <br/> |0x00000001  <br/> |
|NOTIFY_ACCT_CHANGED  <br/> |1  <br/> |
|NOTIFY_ACCT_CREATED  <br/> |segundo  <br/> |
|NOTIFY_ACCT_DELETED  <br/> |3  <br/> |
|NOTIFY_ACCT_ORDER_CHANGED  <br/> |4  <br/> |
|NOTIFY_ACCT_PREDELETED  <br/> |2,5  <br/> |
|OLK_ACCOUNT_NO_FLAGS  <br/> |comprendi  <br/> |
|S_OK  <br/> | *Como se define en el archivo de encabezado Winerror. h de Windows SDK.*  <br/> |
|S_FALSE  <br/> | *Como se define en el archivo de encabezado Winerror. h de Windows SDK.*  <br/> |
|SECURE_FLAG  <br/> |0x8000  <br/> |
|Las siguientes constantes que comienzan con SMTP_ se usan en la propiedad [PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) y especifican el método de autenticación.  <br/> ||
|SMTP_AUTH_SAME_AS_POP  <br/> |comprendi  <br/> |
|SMTP_AUTH_RECEIVE_BEFORE_SEND  <br/> |segundo  <br/> |
|SMTP_AUTH_USER_PASS  <br/> |1  <br/> |
|Las siguientes 5 constantes y macros se usan en la propiedad [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) y especifican opciones para las cuentas pop para dejar una copia de un mensaje en el servidor.  <br/> ||
|LEAVE_ON_SERVER  <br/> |0x1  <br/> |
|REMOVE_AFTER  <br/> |0x2  <br/> |
|REMOVE_ON_NUKE  <br/> |0x4  <br/> |
|GET_REMOVE_AFTER_DAYS (UL)  <br/> |((UL)\>\>16)  <br/> |
|SET_REMOVE_AFTER_DAYS (días)  <br/> |((días)\<\<16)  <br/> |
   
## <a name="class-identifiers"></a>Identificadores de clase

Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef. h de Windows SDK para asociar el nombre simbólico GUID con su valor.
  
{ed475410-b0d6-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAccountManager, 0xed475410, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76); 
  
{ed475411-b0d6-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkPOP3Account, 0xed475411, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{ed475412-b0d6-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkIMAP4Account, 0xed475412, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{ed475414-b0d6-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMAPIAccount, 0xed475414, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{ed475418-b0d6-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMail, 0xed475418, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{ed475419-b0d6-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAddressBook, 0xed475419, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{ed475420-b0d6-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkStore, 0xed475420, 0xb0d6, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{4db5cbf0-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkHotmailAccount, 0x4db5cbf0, 0x3b77, 0x4852, 0xbc, 0x8e, 0xbb, 0x81, 0x90, 0x88, 0x61, 0xf3);
  
{4db5cbf2-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkLDAPAccount, 0x4db5cbf2, 0x3b77, 0x4852, 0xbc, 0x8e, 0xbb, 0x81, 0x90, 0x88, 0x61, 0xf3);
  
## <a name="interface-identifiers"></a>Identificadores de interfaz

Use la macro DEFINE_GUID definida en el archivo de encabezado guiddef. h de Windows SDK para asociar el nombre simbólico GUID con su valor.
  
{9240A6C0-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkErrorUnknown, 0x9240a6c0, 0xaf41, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{9240A6C1-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkEnum, 0x9240a6c1, 0xaf41, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{9240a6c3-af41-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountNotify, 0x9240a6c3, 0xaf41, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  
{9240a6cb-af41-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountHelper, 0x9240a6cb, 0xaf41, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76); 
  
{9240a6cd-af41-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountManager, 0x9240a6cd, 0xaf41, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76); 
  
{9240a6d2-af41-11D2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccount, 0x9240a6d2, 0xaf41, 0x11d2, 0x8c, 0x3b, 0X0, 0x10, 0x4B, 0x2a, 0x66, 0x76);
  

