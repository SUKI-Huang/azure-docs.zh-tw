---
title: "教學課程：Azure Active Directory 與 Proofpoint on Demand 整合 | Microsoft Docs"
description: "了解如何設定 Azure Active Directory 與 Proofpoint on Demand 之間的單一登入。"
services: active-directory
documentationCenter: na
author: jeevansd
manager: femila
ms.assetid: 773e7f7d-ec31-411b-860d-6a6633335d43
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 06/01/2017
ms.author: jeedes
ms.openlocfilehash: b4c8d8c187fc865a905016f04a41843894249f5e
ms.sourcegitcommit: 6699c77dcbd5f8a1a2f21fba3d0a0005ac9ed6b7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/11/2017
---
# <a name="tutorial-azure-active-directory-integration-with-proofpoint-on-demand"></a>教學課程：Azure Active Directory 與 Proofpoint on Demand 整合

在本教學課程中，您會了解如何整合 Proofpoint on Demand 與 Azure Active Directory (Azure AD)。

Proofpoint on Demand 與 Azure AD 整合提供下列優點：

- 您可以在 Azure AD 中控制可存取 Proofpoint on Demand 的人員
- 您可以讓使用者使用他們的 Azure AD 帳戶自動登入 Proofpoint on Demand (單一登入)
- 您可以在 Azure 入口網站中集中管理您的帳戶

如果您想要了解有關 SaaS 應用程式與 Azure AD 之整合的更多詳細資料，請參閱[什麼是搭配 Azure Active Directory 的應用程式存取和單一登入](active-directory-appssoaccess-whatis.md)。

## <a name="prerequisites"></a>必要條件

若要設定 Azure AD 與 Proofpoint on Demand 的整合，您需要下列項目：

- Azure AD 訂用帳戶
- 啟用 Proofpoint on Demand 單一登入的訂用帳戶

> [!NOTE]
> 若要測試本教學課程中的步驟，我們不建議使用生產環境。

若要測試本教學課程中的步驟，您應該遵循這些建議：

- 除非必要，否則請勿使用生產環境。
- 如果您沒有 Azure AD 試用環境，您可以在 [這裡](https://azure.microsoft.com/pricing/free-trial/)取得一個月試用。

## <a name="scenario-description"></a>案例描述
在本教學課程中，您會在測試環境中測試 Azure AD 單一登入。 本教學課程中說明的案例由二個主要建置組塊組成：

1. 從資源庫新增 Proofpoint on Demand
2. 設定並測試 Azure AD 單一登入

## <a name="adding-proofpoint-on-demand-from-the-gallery"></a>從資源庫新增 Proofpoint on Demand
若要設定將 Proofpoint on Demand 整合到 Azure AD 中，您需要從資源庫將 Proofpoint on Demand 新增到受管理的 SaaS 應用程式清單。

**若要從資源庫新增 Proofpoint on Demand，請執行下列步驟：**

1. 在 **[Azure 入口網站](https://portal.azure.com)**的左方瀏覽窗格中，按一下 [Azure Active Directory] 圖示。 

    ![Active Directory][1]

2. 瀏覽至 [企業應用程式]。 然後移至 [所有應用程式]。

    ![應用程式][2]
    
3. 若要新增新的應用程式，請按一下對話方塊頂端的 [新增應用程式] 按鈕。

    ![應用程式][3]

4. 在搜尋方塊中，輸入 **Proofpoint on Demand**。

    ![建立 Azure AD 測試使用者](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_proofpointondemand_search.png)

5. 在結果窗格中，選取 Proofpoint on Demand，然後按一下新增 按鈕，以新增應用程式。

    ![建立 Azure AD 測試使用者](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_proofpointondemand_addfromgallery.png)

##  <a name="configuring-and-testing-azure-ad-single-sign-on"></a>設定並測試 Azure AD 單一登入
在本節中，您會以名為 "Britta Simon" 的測試使用者身分，設定及測試與 Proofpoint on Demand 搭配運作的 Azure AD 單一登入。

若要讓單一登入能夠運作，Azure AD 必須知道 Proofpoint on Demand 與 Azure AD 中互相對應的使用者。 換句話說，您必須建立 Azure AD 使用者和 Proofpoint on Demand 中相關使用者之間的連結關聯性。

建立此連結關聯性的方法，就是將 Azure AD 中 [使用者名稱] 的值指派為 Proofpoint on Demand 中 [使用者名稱] 的值。

若要設定及測試與 Proofpoint on Demand 搭配運作的 Azure AD 單一登入，您需要完成下列建置組塊：

1. **[設定 Azure AD 單一登入](#configuring-azure-ad-single-sign-on)** - 讓您的使用者能夠使用此功能。
2. **[建立 Azure AD 測試使用者](#creating-an-azure-ad-test-user)** - 使用 Britta Simon 測試 Azure AD 單一登入。
3. **[建立 Proofpoint 測試使用者](#creating-a-proofpoint-on-demand-test-user)** - 使 Proofpoint 中 Britta Simon 的對應使用者連結到該使用者在 Azure AD 中的代表身分。
4. **[指派 Azure AD 測試使用者](#assigning-the-azure-ad-test-user)** - 讓 Britta Simon 能夠使用 Azure AD 單一登入。
5. **[Testing Single Sign-On](#testing-single-sign-on)** - 驗證組態是否能運作。

### <a name="configuring-azure-ad-single-sign-on"></a>設定 Azure AD 單一登入

在本節中，您會在 Azure 入口網站中啟用 Azure AD 單一登入，並在您的 Proofpoint on Demand 應用程式中設定單一登入。

**若要使用 Proofpoint on Demand 設定 Azure AD 單一登入，請執行下列步驟：**

1. 在 Azure 入口網站的 [Proofpoint on Demand] 應用程式整合頁面上，按一下 [單一登入]。

    ![設定單一登入][4]

2. 在 [單一登入] 對話方塊上，於 [模式] 選取 [SAML 登入]，以啟用單一登入。
  
    ![設定單一登入](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_proofpointondemand_samlbase.png)

3. 在 [Proofpoint on Demand 網域及 URL] 區段中，執行下列步驟：

    ![設定單一登入](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_proofpointondemand_url.png)

    a. 在 [登入 URL] 文字方塊中，使用下列模式輸入 URL︰`https://<hostname>.pphosted.com/ppssamlsp_hostname`

    b.這是另一個 C# 主控台應用程式。 在 [識別碼] 文字方塊中，使用下列模式輸入 URL：`https://<hostname>.pphosted.com/ppssamlsp`

    c.  在 [回覆 URL] 文字方塊中，以下列模式輸入 URL：`https://<hostname>.pphosted.com:portnumber/v1/samlauth/samlconsumer`
     
    > [!NOTE] 
    > 這些都不是真正的值。 使用實際的識別碼、回覆 URL 和登入 URL 來更新這些值。 請連絡 [Proofpoint on Demand 用戶端支援小組](https://www.proofpoint.com/us/support-services)以取得這些值。 

4. 在 [SAML 簽署憑證] 區段上，按一下 [憑證 (Base64)]，然後將憑證檔案儲存在您的電腦上。

    ![設定單一登入](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_proofpointondemand_certificate.png) 

5. 按一下 [儲存]  按鈕。

    ![設定單一登入](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_400.png)
    
6. 在 [Proofpoint on Demand 組態] 區段中，按一下 [設定 Proofpoint on Demand]，以開啟 [設定登入] 視窗。 從 [快速參考] 區段中複製 **SAML 實體識別碼和 SAML 單一登入服務 URL**。

    ![設定單一登入](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_proofpointondemand_configure.png) 

7. 若要在 **Proofpoint on Demand** 端設定單一登入，您必須將已下載的**憑證 (Base64)**、**SAML 實體識別碼**及 **SAML 單一登入服務 URL** 傳送給 [Proofpoint on Demand 用戶端支援小組](https://www.proofpoint.com/us/support-services)。

> [!TIP]
> 現在，當您設定此應用程式時，在 [Azure 入口網站](https://portal.azure.com)內即可閱讀這些指示的簡要版本！  從 [Active Directory] > [企業應用程式] 區段新增此應用程式之後，只要按一下 [單一登入] 索引標籤，即可透過底部的 [組態] 區段存取內嵌的文件。 您可以從以下連結閱讀更多有關內嵌文件功能的資訊：[Azure AD 內嵌文件]( https://go.microsoft.com/fwlink/?linkid=845985)

### <a name="creating-an-azure-ad-test-user"></a>建立 Azure AD 測試使用者
本節的目標是要在 Azure 入口網站中建立一個名為 Britta Simon 的測試使用者。

![建立 Azure AD 使用者][100]

**若要在 Azure AD 中建立測試使用者，請執行下列步驟：**

1. 在 **Azure 入口網站**的左方瀏覽窗格中，按一下 [Azure Active Directory] 圖示。

    ![建立 Azure AD 測試使用者](./media/active-directory-saas-proofpoint-ondemand-tutorial/create_aaduser_01.png) 

2. 這些都不是真正的值。 使用實際值來更新這些值
    
    ![建立 Azure AD 測試使用者](./media/active-directory-saas-proofpoint-ondemand-tutorial/create_aaduser_02.png) 

3. 若要開啟 [使用者] 對話方塊，按一下對話方塊頂端的 [新增]。
 
    ![建立 Azure AD 測試使用者](./media/active-directory-saas-proofpoint-ondemand-tutorial/create_aaduser_03.png) 

4. 在 [使用者]  對話頁面上，執行下列步驟：
 
    ![建立 Azure AD 測試使用者](./media/active-directory-saas-proofpoint-ondemand-tutorial/create_aaduser_04.png) 

    a. 在 [名稱] 文字方塊中，輸入 **Britta Simon**。

    b.這是另一個 C# 主控台應用程式。 在 [使用者名稱] 文字方塊中，輸入 Britta Simon 的「電子郵件地址」。

    c. 選取 [顯示密碼] 並記下 [密碼] 的值。

    d. 按一下 [建立] 。
 
### <a name="creating-a-proofpoint-on-demand-test-user"></a>建立 Proofpoint on Demand 測試使用者

在本節中，您會在 Proofpoint on Demand 中建立名為 Britta Simon 的使用者。 請與 [Proofpoint on Demand 支援小組](https://www.proofpoint.com/us/support-services)合作，在 Proofpoint on Demand 平台中新增使用者。

### <a name="assigning-the-azure-ad-test-user"></a>指派 Azure AD 測試使用者

在本節中，您會將 Proofpoint on Demand 的存取權授與 Britta Simon，讓 Britta Simon 能夠使用 Azure 單一登入。

![指派使用者][200] 

**若要將 Britta Simon 指派到 Proofpoint on Demand，請執行以下步驟：**

1. 在 Azure 入口網站中，開啟應用程式檢視，接著瀏覽至目錄檢視並移至 [企業應用程式]，然後按一下 [所有應用程式]。

    ![指派使用者][201] 

2. 在應用程式清單中，選取 [Proofpoint on Demand]。

    ![設定單一登入](./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_proofpointondemand_app.png) 

3. 在左側功能表中，按一下 [使用者和群組]。

    ![指派使用者][202] 

4. 按一下 [新增] 按鈕。 然後選取 [新增指派] 對話方塊上的 [使用者和群組]。

    ![指派使用者][203]

5. 在 [使用者和群組] 對話方塊上，選取 [使用者] 清單中的 [Britta Simon]。

6. 按一下 [使用者和群組] 對話方塊上的 [選取] 按鈕。

7. 按一下 [新增指派] 對話方塊上的 [指派] 按鈕。
    
### <a name="testing-single-sign-on"></a>測試單一登入

在本節中，您會使用存取面板來測試您的 Azure AD 單一登入設定。

當您在存取面板上按一下 [Proofpoint on Demand] 圖格時，您應該會自動登入 Proofpoint on Demand 應用程式。
如需「存取面板」的詳細資訊，請參閱[存取面板簡介](active-directory-saas-access-panel-introduction.md)。  

## <a name="additional-resources"></a>其他資源

* [如何與 Azure Active Directory 整合 SaaS 應用程式的教學課程清單](active-directory-saas-tutorial-list.md)
* [什麼是搭配 Azure Active Directory 的應用程式存取和單一登入？](active-directory-appssoaccess-whatis.md)



<!--Image references-->

[1]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_04.png

[100]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_201.png
[202]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_202.png
[203]: ./media/active-directory-saas-proofpoint-ondemand-tutorial/tutorial_general_203.png

